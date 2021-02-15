---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114283"
---
# <span data-ttu-id="0abe1-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="0abe1-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="0abe1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0abe1-102">SYNOPSIS</span></span>
<span data-ttu-id="0abe1-103">Obter cadeia de conexão de um MariaDB em uma determinada estrutura.</span><span class="sxs-lookup"><span data-stu-id="0abe1-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="0abe1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0abe1-104">SYNTAX</span></span>

### <span data-ttu-id="0abe1-105">Nomedo Servidor (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0abe1-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0abe1-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="0abe1-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0abe1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0abe1-107">DESCRIPTION</span></span>
<span data-ttu-id="0abe1-108">Obter cadeia de conexão de um MariaDB em uma determinada estrutura.</span><span class="sxs-lookup"><span data-stu-id="0abe1-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="0abe1-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0abe1-109">EXAMPLES</span></span>

### <span data-ttu-id="0abe1-110">Exemplo 1: Obter uma cadeia de conexão de MariaDB</span><span class="sxs-lookup"><span data-stu-id="0abe1-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="0abe1-111">Esse comando obtém uma cadeia de conexão do MariaDB.</span><span class="sxs-lookup"><span data-stu-id="0abe1-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="0abe1-112">Exemplo 2: Obter uma cadeia de conexão de MariaDB</span><span class="sxs-lookup"><span data-stu-id="0abe1-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="0abe1-113">Esse comando obtém uma cadeia de conexão do MariaDB.</span><span class="sxs-lookup"><span data-stu-id="0abe1-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="0abe1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0abe1-114">PARAMETERS</span></span>

### <span data-ttu-id="0abe1-115">-Cliente</span><span class="sxs-lookup"><span data-stu-id="0abe1-115">-Client</span></span>
<span data-ttu-id="0abe1-116">Tipo de cliente Conectar</span><span class="sxs-lookup"><span data-stu-id="0abe1-116">Connect client type</span></span>

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

### <span data-ttu-id="0abe1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0abe1-117">-DefaultProfile</span></span>
<span data-ttu-id="0abe1-118">região DefaultParameters As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0abe1-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0abe1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0abe1-119">-InputObject</span></span>
<span data-ttu-id="0abe1-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="0abe1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0abe1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0abe1-121">-Name</span></span>
<span data-ttu-id="0abe1-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0abe1-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0abe1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0abe1-123">-ResourceGroupName</span></span>
<span data-ttu-id="0abe1-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="0abe1-124">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0abe1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0abe1-125">-SubscriptionId</span></span>
<span data-ttu-id="0abe1-126">A ID da assinatura faz parte do URI para cada chamada de serviço</span><span class="sxs-lookup"><span data-stu-id="0abe1-126">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0abe1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0abe1-127">CommonParameters</span></span>
<span data-ttu-id="0abe1-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0abe1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0abe1-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0abe1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0abe1-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="0abe1-130">INPUTS</span></span>

### <span data-ttu-id="0abe1-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="0abe1-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0abe1-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="0abe1-132">OUTPUTS</span></span>

### <span data-ttu-id="0abe1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0abe1-133">System.String</span></span>

## <span data-ttu-id="0abe1-134">Notas</span><span class="sxs-lookup"><span data-stu-id="0abe1-134">NOTES</span></span>

<span data-ttu-id="0abe1-135">Aliases</span><span class="sxs-lookup"><span data-stu-id="0abe1-135">ALIASES</span></span>

<span data-ttu-id="0abe1-136">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="0abe1-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0abe1-137">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0abe1-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0abe1-138">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0abe1-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0abe1-139">INPUTOBJECT: <IServer> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="0abe1-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="0abe1-140">`Location <String>`: o local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="0abe1-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="0abe1-141">`[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="0abe1-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="0abe1-142">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="0abe1-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0abe1-143">`[AdministratorLogin <String>]`: o nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="0abe1-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="0abe1-144">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="0abe1-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="0abe1-145">`[EarliestRestoreDate <DateTime?>]`: tempo de criação do ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="0abe1-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="0abe1-146">`[FullyQualifiedDomainName <String>]`: o nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="0abe1-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="0abe1-147">`[IdentityType <IdentityType?>]`: o tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="0abe1-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="0abe1-148">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="0abe1-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="0abe1-149">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="0abe1-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="0abe1-150">`[ReplicaCapacity <Int32?>]`: o número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="0abe1-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="0abe1-151">`[ReplicationRole <String>]`: a função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="0abe1-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="0abe1-152">`[SkuCapacity <Int32?>]`: a capacidade de aumento/reajuste, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="0abe1-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="0abe1-153">`[SkuFamily <String>]`: a família de hardware.</span><span class="sxs-lookup"><span data-stu-id="0abe1-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="0abe1-154">`[SkuName <String>]`: O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0abe1-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="0abe1-155">`[SkuSize <String>]`: o código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="0abe1-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="0abe1-156">`[SkuTier <SkuTier?>]`: o nível da SKU específica, por exemplo, Básico.</span><span class="sxs-lookup"><span data-stu-id="0abe1-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="0abe1-157">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não ao se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="0abe1-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="0abe1-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="0abe1-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="0abe1-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar a redundância geográfica ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="0abe1-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="0abe1-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o crescimento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0abe1-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="0abe1-161">`[StorageProfileStorageMb <Int32?>]`: armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="0abe1-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="0abe1-162">`[UserVisibleState <ServerState?>]`: um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="0abe1-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="0abe1-163">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="0abe1-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="0abe1-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0abe1-164">RELATED LINKS</span></span>

