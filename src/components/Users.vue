<template>
<div class="container mt-4">
	<nav class="navbar navbar-inverse">
	            <div class="container-fluid">
	              <div class="table-navbar-header">
	                <a class="navbar-brand" href="#">Clients</a>
	              </div>
	              <div class="custom-nav">
	                <ul class="nav navbar-nav">
	                    <li class="active"><a href="#">Fund</a></li>
	                     <li class="dropdown">
	                      <a class="dropdown-toggle" data-toggle="dropdown" href="#">Portofolio
	                      <span class="caret"></span></a>
	                      <ul class="dropdown-menu">
	                        <li><a href="#">Page 1-1</a></li>
	                        <li><a href="#">Page 1-2</a></li>
	                        <li><a href="#">Page 1-3</a></li>
	                      </ul>
	                    </li>
	                    <li><a href="#">Client</a></li>
	                    <li><a href="#">Brokers</a></li>
	                    <li><a href="#">Reports</a></li>
	                    <li><a href="#">Logos</a></li>
	                </ul>
	              </div>
	                
	            </div>
	          </nav>   
	          <table class="table table-bordered">
	            <thead>
	              <tr>
	                <th>Client</th>
	                <th>Fund</th>
	                <th>Fund Name</th>
	                <th>Currency</th>
	                <th>Portfolio</th>
	                <th>Type</th>
	                <th>Status</th>
	                <th>Date created</th>
	                <th>Date deactivated</th>
	              </tr>
	            </thead>
	            <tbody>
	              <tr>
	                <td>John</td>
	                <td>Doe</td>
	                <td>Dollar</td>
	                <td>USD</td>
	                <td>Doe</td>
	                <td>A</td>
	                <td>on</td>
	                <td>2016.3.1</td>
	                <td>2016.5.1</td>
	              </tr>
	              <tr>
	                <td>Mary</td>
	                <td>Moe</td>
	                <td>Dollar</td>
	                <td>USD</td>
	                <td>Doe</td>
	                <td>A</td>
	                <td>on</td>
	                <td>2016.3.1</td>
	                <td>2016.5.1</td>
	              </tr>
	              <tr>
	                <td>July</td>
	                <td>Dooley</td> 
	                <td>Dollar</td>
	                <td>USD</td>
	                <td>Doe</td>
	                <td>A</td>
	                <td>on</td>
	                <td>2016.3.1</td>
	                <td>2016.5.1</td>

	              </tr>
	            </tbody>
	          </table>
	      </div>     
</div>
   
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      user_id: '',
      user_pwd: ''
    }
  },
  methods: {
    addUser: function() {
      var userId = this.user_id;
      var userPwd = this.user_pwd;
      this.$http.post('/api/user/addUser', {
        user_id: userId,
        user_pwd: userPwd
      }).then((response) => {
        console.log(response);
      })
    }
  }
}
</script>