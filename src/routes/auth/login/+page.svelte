<script>
    import appAxios from "../../../Api/api.js";
    let email = "";
    let password = "";
    const handleLogin = async () => {
        try {
            const res = await appAxios.post("/login", { email, password });
            console.log(res);
        } catch (error) {
            console.log(error);
        }
    };
</script>

<div>
    <label for="">email</label>
    <input type="text" name="email" bind:value={email} />
    <label for="">password</label>
    <input type="text" name="password" bind:value={password} />
    <button on:click={handleLogin}>login</button>
</div>

<style>
    input {
        border: 1px solid #000;
    }
</style>
