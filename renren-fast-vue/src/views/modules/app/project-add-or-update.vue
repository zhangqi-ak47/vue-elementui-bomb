<template>
  <el-dialog
    :title="!dataForm.id ? '新增' : '修改'"
    :close-on-click-modal="false"
    :visible.sync="visible">
    <el-form :model="dataForm" :rules="dataRule" ref="dataForm" @keyup.enter.native="dataFormSubmit()" label-width="80px">
    <el-form-item label="group_id 123" prop="groupId">
      <el-input v-model="dataForm.groupId" placeholder="group_id 123"></el-input>
    </el-form-item>
    <el-form-item label="plan 数量" prop="plan">
      <el-input v-model="dataForm.plan" placeholder="plan 数量"></el-input>
    </el-form-item>
    <el-form-item label="team 是否属于团队" prop="team">
      <el-input v-model="dataForm.team" placeholder="team 是否属于团队"></el-input>
    </el-form-item>
    <el-form-item label="max_member" prop="maxMember">
      <el-input v-model="dataForm.maxMember" placeholder="max_member"></el-input>
    </el-form-item>
    <el-form-item label="recommended" prop="recommended">
      <el-input v-model="dataForm.recommended" placeholder="recommended"></el-input>
    </el-form-item>
    <el-form-item label="backend_project_path" prop="backendProjectPath">
      <el-input v-model="dataForm.backendProjectPath" placeholder="backend_project_path"></el-input>
    </el-form-item>
    <el-form-item label="name" prop="name">
      <el-input v-model="dataForm.name" placeholder="name"></el-input>
    </el-form-item>
    <el-form-item label="owner_id" prop="ownerId">
      <el-input v-model="dataForm.ownerId" placeholder="owner_id"></el-input>
    </el-form-item>
    <el-form-item label="owner_user_home" prop="ownerUserHome">
      <el-input v-model="dataForm.ownerUserHome" placeholder="owner_user_home"></el-input>
    </el-form-item>
    <el-form-item label="owner_user_name" prop="ownerUserName">
      <el-input v-model="dataForm.ownerUserName" placeholder="owner_user_name"></el-input>
    </el-form-item>
    <el-form-item label="owner_user_picture" prop="ownerUserPicture">
      <el-input v-model="dataForm.ownerUserPicture" placeholder="owner_user_picture"></el-input>
    </el-form-item>
    <el-form-item label="project_path" prop="projectPath">
      <el-input v-model="dataForm.projectPath" placeholder="project_path"></el-input>
    </el-form-item>
    <el-form-item label="ssh_url" prop="sshUrl">
      <el-input v-model="dataForm.sshUrl" placeholder="ssh_url"></el-input>
    </el-form-item>
    <el-form-item label="current_user_role" prop="currentUserRole">
      <el-input v-model="dataForm.currentUserRole" placeholder="current_user_role"></el-input>
    </el-form-item>
    <el-form-item label="current_user_role_id" prop="currentUserRoleId">
      <el-input v-model="dataForm.currentUserRoleId" placeholder="current_user_role_id"></el-input>
    </el-form-item>
    <el-form-item label="depot_path" prop="depotPath">
      <el-input v-model="dataForm.depotPath" placeholder="depot_path"></el-input>
    </el-form-item>
    <el-form-item label="description" prop="description">
      <el-input v-model="dataForm.description" placeholder="description"></el-input>
    </el-form-item>
    <el-form-item label="git_url" prop="gitUrl">
      <el-input v-model="dataForm.gitUrl" placeholder="git_url"></el-input>
    </el-form-item>
    <el-form-item label="https_url" prop="httpsUrl">
      <el-input v-model="dataForm.httpsUrl" placeholder="https_url"></el-input>
    </el-form-item>
    <el-form-item label="icon" prop="icon">
      <el-input v-model="dataForm.icon" placeholder="icon"></el-input>
    </el-form-item>
    <el-form-item label="fork_count" prop="forkCount">
      <el-input v-model="dataForm.forkCount" placeholder="fork_count"></el-input>
    </el-form-item>
    <el-form-item label="forked状态  0：禁用   1：正常" prop="forked">
      <el-input v-model="dataForm.forked" placeholder="forked状态  0：禁用   1：正常"></el-input>
    </el-form-item>
    <el-form-item label="created_at" prop="createdAt">
      <el-input v-model="dataForm.createdAt" placeholder="created_at"></el-input>
    </el-form-item>
    <el-form-item label="star_count" prop="starCount">
      <el-input v-model="dataForm.starCount" placeholder="star_count"></el-input>
    </el-form-item>
    <el-form-item label="stared" prop="stared">
      <el-input v-model="dataForm.stared" placeholder="stared"></el-input>
    </el-form-item>
    <el-form-item label="status测试  0：false   1：true" prop="status">
      <el-input v-model="dataForm.status" placeholder="status测试  0：false   1：true"></el-input>
    </el-form-item>
    <el-form-item label="un_read_activities_count" prop="unReadActivitiesCount">
      <el-input v-model="dataForm.unReadActivitiesCount" placeholder="un_read_activities_count"></el-input>
    </el-form-item>
    <el-form-item label="update_at" prop="updateAt">
      <el-input v-model="dataForm.updateAt" placeholder="update_at"></el-input>
    </el-form-item>
    <el-form-item label="watch_count" prop="watchCount">
      <el-input v-model="dataForm.watchCount" placeholder="watch_count"></el-input>
    </el-form-item>
    <el-form-item label="watched" prop="watched">
      <el-input v-model="dataForm.watched" placeholder="watched"></el-input>
    </el-form-item>
    <el-form-item label="is_public" prop="isPublic">
      <el-input v-model="dataForm.isPublic" placeholder="is_public"></el-input>
    </el-form-item>
    <el-form-item label="member_num" prop="memberNum">
      <el-input v-model="dataForm.memberNum" placeholder="member_num"></el-input>
    </el-form-item>
    <el-form-item label="pin" prop="pin">
      <el-input v-model="dataForm.pin" placeholder="pin"></el-input>
    </el-form-item>
    <el-form-item label="type" prop="type">
      <el-input v-model="dataForm.type" placeholder="type"></el-input>
    </el-form-item>
    <el-form-item label="shared" prop="shared">
      <el-input v-model="dataForm.shared" placeholder="shared"></el-input>
    </el-form-item>
    <el-form-item label="fork_path" prop="forkPath">
      <el-input v-model="dataForm.forkPath" placeholder="fork_path"></el-input>
    </el-form-item>
    </el-form>
    <span slot="footer" class="dialog-footer">
      <el-button @click="visible = false">取消</el-button>
      <el-button type="primary" @click="dataFormSubmit()">确定</el-button>
    </span>
  </el-dialog>
</template>

<script>
  export default {
    data () {
      return {
        visible: false,
        dataForm: {
          id: 0,
          groupId: '',
          plan: '',
          team: '',
          maxMember: '',
          recommended: '',
          backendProjectPath: '',
          name: '',
          ownerId: '',
          ownerUserHome: '',
          ownerUserName: '',
          ownerUserPicture: '',
          projectPath: '',
          sshUrl: '',
          currentUserRole: '',
          currentUserRoleId: '',
          depotPath: '',
          description: '',
          gitUrl: '',
          httpsUrl: '',
          icon: '',
          forkCount: '',
          forked: '',
          createdAt: '',
          starCount: '',
          stared: '',
          status: '',
          unReadActivitiesCount: '',
          updateAt: '',
          watchCount: '',
          watched: '',
          isPublic: '',
          memberNum: '',
          pin: '',
          type: '',
          shared: '',
          forkPath: ''
        },
        dataRule: {
          groupId: [
            { required: true, message: 'group_id 123不能为空', trigger: 'blur' }
          ],
          plan: [
            { required: true, message: 'plan 数量不能为空', trigger: 'blur' }
          ],
          team: [
            { required: true, message: 'team 是否属于团队不能为空', trigger: 'blur' }
          ],
          maxMember: [
            { required: true, message: 'max_member不能为空', trigger: 'blur' }
          ],
          recommended: [
            { required: true, message: 'recommended不能为空', trigger: 'blur' }
          ],
          backendProjectPath: [
            { required: true, message: 'backend_project_path不能为空', trigger: 'blur' }
          ],
          name: [
            { required: true, message: 'name不能为空', trigger: 'blur' }
          ],
          ownerId: [
            { required: true, message: 'owner_id不能为空', trigger: 'blur' }
          ],
          ownerUserHome: [
            { required: true, message: 'owner_user_home不能为空', trigger: 'blur' }
          ],
          ownerUserName: [
            { required: true, message: 'owner_user_name不能为空', trigger: 'blur' }
          ],
          ownerUserPicture: [
            { required: true, message: 'owner_user_picture不能为空', trigger: 'blur' }
          ],
          projectPath: [
            { required: true, message: 'project_path不能为空', trigger: 'blur' }
          ],
          sshUrl: [
            { required: true, message: 'ssh_url不能为空', trigger: 'blur' }
          ],
          currentUserRole: [
            { required: true, message: 'current_user_role不能为空', trigger: 'blur' }
          ],
          currentUserRoleId: [
            { required: true, message: 'current_user_role_id不能为空', trigger: 'blur' }
          ],
          depotPath: [
            { required: true, message: 'depot_path不能为空', trigger: 'blur' }
          ],
          description: [
            { required: true, message: 'description不能为空', trigger: 'blur' }
          ],
          gitUrl: [
            { required: true, message: 'git_url不能为空', trigger: 'blur' }
          ],
          httpsUrl: [
            { required: true, message: 'https_url不能为空', trigger: 'blur' }
          ],
          icon: [
            { required: true, message: 'icon不能为空', trigger: 'blur' }
          ],
          forkCount: [
            { required: true, message: 'fork_count不能为空', trigger: 'blur' }
          ],
          forked: [
            { required: true, message: 'forked状态  0：禁用   1：正常不能为空', trigger: 'blur' }
          ],
          createdAt: [
            { required: true, message: 'created_at不能为空', trigger: 'blur' }
          ],
          starCount: [
            { required: true, message: 'star_count不能为空', trigger: 'blur' }
          ],
          stared: [
            { required: true, message: 'stared不能为空', trigger: 'blur' }
          ],
          status: [
            { required: true, message: 'status测试  0：false   1：true不能为空', trigger: 'blur' }
          ],
          unReadActivitiesCount: [
            { required: true, message: 'un_read_activities_count不能为空', trigger: 'blur' }
          ],
          updateAt: [
            { required: true, message: 'update_at不能为空', trigger: 'blur' }
          ],
          watchCount: [
            { required: true, message: 'watch_count不能为空', trigger: 'blur' }
          ],
          watched: [
            { required: true, message: 'watched不能为空', trigger: 'blur' }
          ],
          isPublic: [
            { required: true, message: 'is_public不能为空', trigger: 'blur' }
          ],
          memberNum: [
            { required: true, message: 'member_num不能为空', trigger: 'blur' }
          ],
          pin: [
            { required: true, message: 'pin不能为空', trigger: 'blur' }
          ],
          type: [
            { required: true, message: 'type不能为空', trigger: 'blur' }
          ],
          shared: [
            { required: true, message: 'shared不能为空', trigger: 'blur' }
          ],
          forkPath: [
            { required: true, message: 'fork_path不能为空', trigger: 'blur' }
          ]
        }
      }
    },
    methods: {
      init (id) {
        this.dataForm.id = id || 0
        this.visible = true
        this.$nextTick(() => {
          this.$refs['dataForm'].resetFields()
          if (this.dataForm.id) {
            this.$http({
              url: this.$http.adornUrl(`/app/project/info/${this.dataForm.id}`),
              method: 'get',
              params: this.$http.adornParams()
            }).then(({data}) => {
              if (data && data.code === 0) {
                this.dataForm.groupId = data.project.groupId
                this.dataForm.plan = data.project.plan
                this.dataForm.team = data.project.team
                this.dataForm.maxMember = data.project.maxMember
                this.dataForm.recommended = data.project.recommended
                this.dataForm.backendProjectPath = data.project.backendProjectPath
                this.dataForm.name = data.project.name
                this.dataForm.ownerId = data.project.ownerId
                this.dataForm.ownerUserHome = data.project.ownerUserHome
                this.dataForm.ownerUserName = data.project.ownerUserName
                this.dataForm.ownerUserPicture = data.project.ownerUserPicture
                this.dataForm.projectPath = data.project.projectPath
                this.dataForm.sshUrl = data.project.sshUrl
                this.dataForm.currentUserRole = data.project.currentUserRole
                this.dataForm.currentUserRoleId = data.project.currentUserRoleId
                this.dataForm.depotPath = data.project.depotPath
                this.dataForm.description = data.project.description
                this.dataForm.gitUrl = data.project.gitUrl
                this.dataForm.httpsUrl = data.project.httpsUrl
                this.dataForm.icon = data.project.icon
                this.dataForm.forkCount = data.project.forkCount
                this.dataForm.forked = data.project.forked
                this.dataForm.createdAt = data.project.createdAt
                this.dataForm.starCount = data.project.starCount
                this.dataForm.stared = data.project.stared
                this.dataForm.status = data.project.status
                this.dataForm.unReadActivitiesCount = data.project.unReadActivitiesCount
                this.dataForm.updateAt = data.project.updateAt
                this.dataForm.watchCount = data.project.watchCount
                this.dataForm.watched = data.project.watched
                this.dataForm.isPublic = data.project.isPublic
                this.dataForm.memberNum = data.project.memberNum
                this.dataForm.pin = data.project.pin
                this.dataForm.type = data.project.type
                this.dataForm.shared = data.project.shared
                this.dataForm.forkPath = data.project.forkPath
              }
            })
          }
        })
      },
      // 表单提交
      dataFormSubmit () {
        this.$refs['dataForm'].validate((valid) => {
          if (valid) {
            this.$http({
              url: this.$http.adornUrl(`/app/project/${!this.dataForm.id ? 'save' : 'update'}`),
              method: 'post',
              data: this.$http.adornData({
                'id': this.dataForm.id || undefined,
                'groupId': this.dataForm.groupId,
                'plan': this.dataForm.plan,
                'team': this.dataForm.team,
                'maxMember': this.dataForm.maxMember,
                'recommended': this.dataForm.recommended,
                'backendProjectPath': this.dataForm.backendProjectPath,
                'name': this.dataForm.name,
                'ownerId': this.dataForm.ownerId,
                'ownerUserHome': this.dataForm.ownerUserHome,
                'ownerUserName': this.dataForm.ownerUserName,
                'ownerUserPicture': this.dataForm.ownerUserPicture,
                'projectPath': this.dataForm.projectPath,
                'sshUrl': this.dataForm.sshUrl,
                'currentUserRole': this.dataForm.currentUserRole,
                'currentUserRoleId': this.dataForm.currentUserRoleId,
                'depotPath': this.dataForm.depotPath,
                'description': this.dataForm.description,
                'gitUrl': this.dataForm.gitUrl,
                'httpsUrl': this.dataForm.httpsUrl,
                'icon': this.dataForm.icon,
                'forkCount': this.dataForm.forkCount,
                'forked': this.dataForm.forked,
                'createdAt': this.dataForm.createdAt,
                'starCount': this.dataForm.starCount,
                'stared': this.dataForm.stared,
                'status': this.dataForm.status,
                'unReadActivitiesCount': this.dataForm.unReadActivitiesCount,
                'updateAt': this.dataForm.updateAt,
                'watchCount': this.dataForm.watchCount,
                'watched': this.dataForm.watched,
                'isPublic': this.dataForm.isPublic,
                'memberNum': this.dataForm.memberNum,
                'pin': this.dataForm.pin,
                'type': this.dataForm.type,
                'shared': this.dataForm.shared,
                'forkPath': this.dataForm.forkPath
              })
            }).then(({data}) => {
              if (data && data.code === 0) {
                this.$message({
                  message: '操作成功',
                  type: 'success',
                  duration: 1500,
                  onClose: () => {
                    this.visible = false
                    this.$emit('refreshDataList')
                  }
                })
              } else {
                this.$message.error(data.msg)
              }
            })
          }
        })
      }
    }
  }
</script>
