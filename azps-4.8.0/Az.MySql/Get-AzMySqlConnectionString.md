---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: ab2e820ec0e1c943cfeb5f8b3d83babece38ed95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113481"
---
# <span data-ttu-id="bdf66-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="bdf66-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="bdf66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdf66-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf66-103">Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="bdf66-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="bdf66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdf66-104">SYNTAX</span></span>

### <span data-ttu-id="bdf66-105">Get (padrão)</span><span class="sxs-lookup"><span data-stu-id="bdf66-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bdf66-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bdf66-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdf66-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdf66-107">DESCRIPTION</span></span>
<span data-ttu-id="bdf66-108">Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="bdf66-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="bdf66-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdf66-109">EXAMPLES</span></span>

### <span data-ttu-id="bdf66-110">Exemplo 1: obter cadeia de conexão do servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="bdf66-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="bdf66-111">Este cmdlet obtém a cadeia de conexão do servidor MySql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="bdf66-112">Exemplo 2: obter a cadeia de conexão do servidor MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="bdf66-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="bdf66-113">Esse cmdlet obtém a cadeia de conexão do servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="bdf66-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="bdf66-114">OS</span><span class="sxs-lookup"><span data-stu-id="bdf66-114">PARAMETERS</span></span>

### <span data-ttu-id="bdf66-115">-Cliente</span><span class="sxs-lookup"><span data-stu-id="bdf66-115">-Client</span></span>
<span data-ttu-id="bdf66-116">Provedor de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="bdf66-116">Client connection provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf66-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf66-117">-DefaultProfile</span></span>
<span data-ttu-id="bdf66-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf66-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf66-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdf66-119">-InputObject</span></span>
<span data-ttu-id="bdf66-120">O objeto do servidor de origem do qual criar a réplica.</span><span class="sxs-lookup"><span data-stu-id="bdf66-120">The source server object to create replica from.</span></span>
<span data-ttu-id="bdf66-121">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bdf66-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf66-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdf66-122">-Name</span></span>
<span data-ttu-id="bdf66-123">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdf66-124">-ResourceGroupName</span></span>
<span data-ttu-id="bdf66-125">O nome do grupo de recursos que contém o recurso, você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="bdf66-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf66-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdf66-126">-SubscriptionId</span></span>
<span data-ttu-id="bdf66-127">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf66-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf66-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf66-128">CommonParameters</span></span>
<span data-ttu-id="bdf66-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf66-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf66-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdf66-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf66-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdf66-131">INPUTS</span></span>

### <span data-ttu-id="bdf66-132">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="bdf66-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="bdf66-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdf66-133">OUTPUTS</span></span>

### <span data-ttu-id="bdf66-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bdf66-134">System.String</span></span>

## <span data-ttu-id="bdf66-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdf66-135">NOTES</span></span>

<span data-ttu-id="bdf66-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bdf66-136">ALIASES</span></span>

<span data-ttu-id="bdf66-137">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="bdf66-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bdf66-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="bdf66-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bdf66-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bdf66-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bdf66-140">INPUTobject <IServer> : o objeto do servidor de origem para o qual criar a réplica.</span><span class="sxs-lookup"><span data-stu-id="bdf66-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="bdf66-141">`Location <String>`: O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="bdf66-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="bdf66-142">`[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="bdf66-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="bdf66-143">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="bdf66-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bdf66-144">`[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="bdf66-145">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="bdf66-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="bdf66-146">`[EarliestRestoreDate <DateTime?>]`: Hora de criação do ponto de restauração mais antiga (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="bdf66-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="bdf66-147">`[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="bdf66-148">`[IdentityType <IdentityType?>]`: O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="bdf66-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="bdf66-149">Defina como "SystemAssigned" para criar e atribuir automaticamente uma entidade de segurança do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="bdf66-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="bdf66-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status que mostra se o servidor habilitou a criptografia de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="bdf66-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="bdf66-151">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="bdf66-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="bdf66-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Impor uma versão do TLS mínima para o servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="bdf66-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se o acesso à rede pública é ou não permitido para este servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="bdf66-154">O valor é opcional, mas se transmitido, deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="bdf66-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="bdf66-155">`[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="bdf66-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="bdf66-156">`[ReplicationRole <String>]`: A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="bdf66-157">`[SkuCapacity <Int32?>]`: A capacidade de dimensionamento/saída, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="bdf66-158">`[SkuFamily <String>]`: A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="bdf66-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="bdf66-159">`[SkuName <String>]`: O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bdf66-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="bdf66-160">`[SkuSize <String>]`: O código de tamanho a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="bdf66-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="bdf66-161">`[SkuTier <SkuTier?>]`: A camada do SKU específico, por exemplo, básico.</span><span class="sxs-lookup"><span data-stu-id="bdf66-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="bdf66-162">`[SslEnforcement <SslEnforcementEnum?>]`: Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="bdf66-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="bdf66-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilite a redundância geográfica ou não para o backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="bdf66-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdf66-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="bdf66-166">`[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="bdf66-167">`[UserVisibleState <ServerState?>]`: Um estado de um servidor que é visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="bdf66-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="bdf66-168">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="bdf66-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="bdf66-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdf66-169">RELATED LINKS</span></span>

