---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: c85ece43045144d0befd6a6ed1e7ac1d7431796f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892958"
---
# <span data-ttu-id="0f189-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="0f189-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="0f189-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f189-102">SYNOPSIS</span></span>
<span data-ttu-id="0f189-103">Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="0f189-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="0f189-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0f189-104">SYNTAX</span></span>

### <span data-ttu-id="0f189-105">Get (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0f189-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0f189-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0f189-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f189-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0f189-107">DESCRIPTION</span></span>
<span data-ttu-id="0f189-108">Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="0f189-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="0f189-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f189-109">EXAMPLES</span></span>

### <span data-ttu-id="0f189-110">Exemplo 1: Obter a cadeia de conexão do servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="0f189-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="0f189-111">Este cmdlet obtém a cadeia de conexão do servidor MySql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="0f189-112">Exemplo 2: Obter a cadeia de conexão do servidor MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="0f189-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="0f189-113">Este cmdlet obtém a cadeia de conexão do servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="0f189-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="0f189-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0f189-114">PARAMETERS</span></span>

### <span data-ttu-id="0f189-115">-Client</span><span class="sxs-lookup"><span data-stu-id="0f189-115">-Client</span></span>
<span data-ttu-id="0f189-116">Provedor de conexão de cliente.</span><span class="sxs-lookup"><span data-stu-id="0f189-116">Client connection provider.</span></span>

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

### <span data-ttu-id="0f189-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f189-117">-DefaultProfile</span></span>
<span data-ttu-id="0f189-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f189-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f189-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f189-119">-InputObject</span></span>
<span data-ttu-id="0f189-120">O servidor para a cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="0f189-120">The server for the connection string.</span></span>
<span data-ttu-id="0f189-121">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0f189-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0f189-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0f189-122">-Name</span></span>
<span data-ttu-id="0f189-123">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-123">The name of the server.</span></span>

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

### <span data-ttu-id="0f189-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f189-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f189-125">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="0f189-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0f189-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f189-126">-SubscriptionId</span></span>
<span data-ttu-id="0f189-127">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f189-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="0f189-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f189-128">CommonParameters</span></span>
<span data-ttu-id="0f189-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f189-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f189-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f189-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f189-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f189-131">INPUTS</span></span>

### <span data-ttu-id="0f189-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="0f189-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0f189-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0f189-133">OUTPUTS</span></span>

### <span data-ttu-id="0f189-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0f189-134">System.String</span></span>

## <span data-ttu-id="0f189-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="0f189-135">NOTES</span></span>

<span data-ttu-id="0f189-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0f189-136">ALIASES</span></span>

<span data-ttu-id="0f189-137">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="0f189-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f189-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0f189-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f189-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f189-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f189-140">INPUTOBJECT <IServer> : o servidor para a cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="0f189-140">INPUTOBJECT <IServer>: The server for the connection string.</span></span>
  - <span data-ttu-id="0f189-141">`Location <String>`: A localização geográfica onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="0f189-141">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="0f189-142">`[Tag <ITrackedResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="0f189-142">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="0f189-143">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="0f189-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0f189-144">`[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="0f189-145">Só pode ser especificado quando o servidor está sendo criado (e é necessário para a criação).</span><span class="sxs-lookup"><span data-stu-id="0f189-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="0f189-146">`[EarliestRestoreDate <DateTime?>]`: Tempo de criação de ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="0f189-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="0f189-147">`[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="0f189-148">`[IdentityType <IdentityType?>]`: O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="0f189-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="0f189-149">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="0f189-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="0f189-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status mostrando se a criptografia de infraestrutura habilitada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="0f189-151">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="0f189-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="0f189-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Impor uma versão Tls mínima para o servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="0f189-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se o acesso à rede pública é permitido ou não para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="0f189-154">O valor é opcional, mas, se passado, deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="0f189-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="0f189-155">`[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="0f189-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="0f189-156">`[ReplicationRole <String>]`: A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="0f189-157">`[SkuCapacity <Int32?>]`: A capacidade de dimensionar/sair, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="0f189-158">`[SkuFamily <String>]`: A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="0f189-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="0f189-159">`[SkuName <String>]`: O nome do sku, normalmente, camada + família + núcleos, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0f189-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="0f189-160">`[SkuSize <String>]`: O código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="0f189-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="0f189-161">`[SkuTier <SkuTier?>]`: A camada da SKU específica, por exemplo, Basic.</span><span class="sxs-lookup"><span data-stu-id="0f189-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="0f189-162">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="0f189-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="0f189-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar geo redundante ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="0f189-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o Crescimento Automático de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0f189-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="0f189-166">`[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="0f189-167">`[UserVisibleState <ServerState?>]`: Um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="0f189-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="0f189-168">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="0f189-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="0f189-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f189-169">RELATED LINKS</span></span>

