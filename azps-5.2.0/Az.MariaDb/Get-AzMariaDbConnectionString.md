---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256866"
---
# <span data-ttu-id="aa85d-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="aa85d-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="aa85d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa85d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa85d-103">Obtenha a cadeia de conexão de um MariaDB em uma determinada estrutura.</span><span class="sxs-lookup"><span data-stu-id="aa85d-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="aa85d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa85d-104">SYNTAX</span></span>

### <span data-ttu-id="aa85d-105">ServerName (padrão)</span><span class="sxs-lookup"><span data-stu-id="aa85d-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aa85d-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="aa85d-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa85d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa85d-107">DESCRIPTION</span></span>
<span data-ttu-id="aa85d-108">Obtenha a cadeia de conexão de um MariaDB em uma determinada estrutura.</span><span class="sxs-lookup"><span data-stu-id="aa85d-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="aa85d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa85d-109">EXAMPLES</span></span>

### <span data-ttu-id="aa85d-110">Exemplo 1: obter uma cadeia de conexão de MariaDB</span><span class="sxs-lookup"><span data-stu-id="aa85d-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="aa85d-111">Esse comando obtém uma cadeia de conexão de MariaDB.</span><span class="sxs-lookup"><span data-stu-id="aa85d-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="aa85d-112">Exemplo 2: obter uma cadeia de conexão de MariaDB</span><span class="sxs-lookup"><span data-stu-id="aa85d-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="aa85d-113">Esse comando obtém uma cadeia de conexão de MariaDB.</span><span class="sxs-lookup"><span data-stu-id="aa85d-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="aa85d-114">OS</span><span class="sxs-lookup"><span data-stu-id="aa85d-114">PARAMETERS</span></span>

### <span data-ttu-id="aa85d-115">-Cliente</span><span class="sxs-lookup"><span data-stu-id="aa85d-115">-Client</span></span>
<span data-ttu-id="aa85d-116">Conectar o tipo de cliente</span><span class="sxs-lookup"><span data-stu-id="aa85d-116">Connect client type</span></span>

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

### <span data-ttu-id="aa85d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa85d-117">-DefaultProfile</span></span>
<span data-ttu-id="aa85d-118">Region Defaultparameters as credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa85d-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa85d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa85d-119">-InputObject</span></span>
<span data-ttu-id="aa85d-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="aa85d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa85d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa85d-121">-Name</span></span>
<span data-ttu-id="aa85d-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="aa85d-122">The name of the server.</span></span>

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

### <span data-ttu-id="aa85d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa85d-123">-ResourceGroupName</span></span>
<span data-ttu-id="aa85d-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="aa85d-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="aa85d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa85d-125">-SubscriptionId</span></span>
<span data-ttu-id="aa85d-126">A ID da assinatura faz parte do URI para cada chamada de serviço</span><span class="sxs-lookup"><span data-stu-id="aa85d-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="aa85d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa85d-127">CommonParameters</span></span>
<span data-ttu-id="aa85d-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa85d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa85d-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa85d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa85d-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa85d-130">INPUTS</span></span>

### <span data-ttu-id="aa85d-131">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="aa85d-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="aa85d-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa85d-132">OUTPUTS</span></span>

### <span data-ttu-id="aa85d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="aa85d-133">System.String</span></span>

## <span data-ttu-id="aa85d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa85d-134">NOTES</span></span>

<span data-ttu-id="aa85d-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="aa85d-135">ALIASES</span></span>

<span data-ttu-id="aa85d-136">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="aa85d-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa85d-137">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="aa85d-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa85d-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aa85d-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa85d-139">INPUTobject <IServer> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="aa85d-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="aa85d-140">`Location <String>`: O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="aa85d-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="aa85d-141">`[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="aa85d-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="aa85d-142">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="aa85d-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="aa85d-143">`[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="aa85d-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="aa85d-144">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="aa85d-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="aa85d-145">`[EarliestRestoreDate <DateTime?>]`: Hora de criação do ponto de restauração mais antiga (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="aa85d-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="aa85d-146">`[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="aa85d-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="aa85d-147">`[IdentityType <IdentityType?>]`: O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="aa85d-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="aa85d-148">Defina como "SystemAssigned" para criar e atribuir automaticamente uma entidade de segurança do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="aa85d-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="aa85d-149">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="aa85d-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="aa85d-150">`[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="aa85d-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="aa85d-151">`[ReplicationRole <String>]`: A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="aa85d-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="aa85d-152">`[SkuCapacity <Int32?>]`: A capacidade de dimensionamento/saída, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="aa85d-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="aa85d-153">`[SkuFamily <String>]`: A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="aa85d-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="aa85d-154">`[SkuName <String>]`: O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="aa85d-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="aa85d-155">`[SkuSize <String>]`: O código de tamanho a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="aa85d-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="aa85d-156">`[SkuTier <SkuTier?>]`: A camada do SKU específico, por exemplo, básico.</span><span class="sxs-lookup"><span data-stu-id="aa85d-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="aa85d-157">`[SslEnforcement <SslEnforcementEnum?>]`: Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="aa85d-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="aa85d-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="aa85d-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="aa85d-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilite a redundância geográfica ou não para o backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="aa85d-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="aa85d-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aa85d-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="aa85d-161">`[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="aa85d-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="aa85d-162">`[UserVisibleState <ServerState?>]`: Um estado de um servidor que é visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="aa85d-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="aa85d-163">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="aa85d-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="aa85d-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa85d-164">RELATED LINKS</span></span>

