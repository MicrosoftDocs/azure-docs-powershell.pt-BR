---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: 65eb0d924391e6e12b3b81ac487b746e1b91fa94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114756"
---
# <span data-ttu-id="ad067-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="ad067-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="ad067-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad067-102">SYNOPSIS</span></span>
<span data-ttu-id="ad067-103">Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="ad067-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="ad067-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad067-104">SYNTAX</span></span>

### <span data-ttu-id="ad067-105">Obter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ad067-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ad067-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ad067-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad067-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad067-107">DESCRIPTION</span></span>
<span data-ttu-id="ad067-108">Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="ad067-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="ad067-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ad067-109">EXAMPLES</span></span>

### <span data-ttu-id="ad067-110">Exemplo 1: Obter cadeia de conexão do servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="ad067-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="ad067-111">Este cmdlet obtém a cadeia de conexão do servidor MySql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="ad067-112">Exemplo 2: Obter a cadeia de conexão do servidor MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="ad067-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="ad067-113">Este cmdlet obtém a cadeia de conexão do servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="ad067-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="ad067-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad067-114">PARAMETERS</span></span>

### <span data-ttu-id="ad067-115">-Cliente</span><span class="sxs-lookup"><span data-stu-id="ad067-115">-Client</span></span>
<span data-ttu-id="ad067-116">Provedor de conexão de cliente.</span><span class="sxs-lookup"><span data-stu-id="ad067-116">Client connection provider.</span></span>

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

### <span data-ttu-id="ad067-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad067-117">-DefaultProfile</span></span>
<span data-ttu-id="ad067-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad067-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad067-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad067-119">-InputObject</span></span>
<span data-ttu-id="ad067-120">O servidor para a cadeia de conexão.</span><span class="sxs-lookup"><span data-stu-id="ad067-120">The server for the connection string.</span></span>
<span data-ttu-id="ad067-121">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ad067-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad067-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad067-122">-Name</span></span>
<span data-ttu-id="ad067-123">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-123">The name of the server.</span></span>

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

### <span data-ttu-id="ad067-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad067-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad067-125">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="ad067-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ad067-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad067-126">-SubscriptionId</span></span>
<span data-ttu-id="ad067-127">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad067-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ad067-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad067-128">CommonParameters</span></span>
<span data-ttu-id="ad067-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad067-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad067-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad067-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad067-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="ad067-131">INPUTS</span></span>

### <span data-ttu-id="ad067-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="ad067-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ad067-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="ad067-133">OUTPUTS</span></span>

### <span data-ttu-id="ad067-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ad067-134">System.String</span></span>

## <span data-ttu-id="ad067-135">Notas</span><span class="sxs-lookup"><span data-stu-id="ad067-135">NOTES</span></span>

<span data-ttu-id="ad067-136">Aliases</span><span class="sxs-lookup"><span data-stu-id="ad067-136">ALIASES</span></span>

<span data-ttu-id="ad067-137">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="ad067-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad067-138">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ad067-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad067-139">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad067-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad067-140">INPUTOBJECT: <IServer> o servidor para a cadeia de conexão.</span><span class="sxs-lookup"><span data-stu-id="ad067-140">INPUTOBJECT <IServer>: The server for the connection string.</span></span>
  - <span data-ttu-id="ad067-141">`Location <String>`: a localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="ad067-141">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="ad067-142">`[Tag <ITrackedResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ad067-142">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ad067-143">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="ad067-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ad067-144">`[AdministratorLogin <String>]`: o nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="ad067-145">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="ad067-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="ad067-146">`[EarliestRestoreDate <DateTime?>]`: tempo de criação do ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="ad067-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="ad067-147">`[FullyQualifiedDomainName <String>]`: o nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="ad067-148">`[IdentityType <IdentityType?>]`: o tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="ad067-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="ad067-149">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="ad067-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="ad067-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status mostrando se a criptografia de infraestrutura habilitada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="ad067-151">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="ad067-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="ad067-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Impor uma versão TLs mínima para o servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="ad067-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se o acesso à rede pública é permitido ou não para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="ad067-154">O valor é opcional, mas, se aprovado, deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="ad067-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="ad067-155">`[ReplicaCapacity <Int32?>]`: o número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="ad067-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="ad067-156">`[ReplicationRole <String>]`: a função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="ad067-157">`[SkuCapacity <Int32?>]`: a capacidade de aumento/reajuste, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="ad067-158">`[SkuFamily <String>]`: a família de hardware.</span><span class="sxs-lookup"><span data-stu-id="ad067-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="ad067-159">`[SkuName <String>]`: O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ad067-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="ad067-160">`[SkuSize <String>]`: o código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="ad067-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="ad067-161">`[SkuTier <SkuTier?>]`: o nível da SKU específica, por exemplo, Básico.</span><span class="sxs-lookup"><span data-stu-id="ad067-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="ad067-162">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não ao se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="ad067-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="ad067-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar a redundância geográfica ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="ad067-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o crescimento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ad067-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="ad067-166">`[StorageProfileStorageMb <Int32?>]`: armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="ad067-167">`[UserVisibleState <ServerState?>]`: um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ad067-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="ad067-168">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="ad067-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="ad067-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad067-169">RELATED LINKS</span></span>

