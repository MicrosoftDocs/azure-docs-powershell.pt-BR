---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428260"
---
# <span data-ttu-id="311d1-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="311d1-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="311d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="311d1-102">SYNOPSIS</span></span>
<span data-ttu-id="311d1-103">Obtém os detalhes de uma malha de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="311d1-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="311d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="311d1-104">SYNTAX</span></span>

### <span data-ttu-id="311d1-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="311d1-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="311d1-106">Obter</span><span class="sxs-lookup"><span data-stu-id="311d1-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="311d1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="311d1-107">DESCRIPTION</span></span>
<span data-ttu-id="311d1-108">Obtém os detalhes de uma malha de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="311d1-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="311d1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="311d1-109">EXAMPLES</span></span>

### <span data-ttu-id="311d1-110">Exemplo 1: obter todas as malhas por grupo de recursos e nome do cofre</span><span class="sxs-lookup"><span data-stu-id="311d1-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="311d1-111">Obter todas as malhas no grupo de recursos e no cofre</span><span class="sxs-lookup"><span data-stu-id="311d1-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="311d1-112">Exemplo 2: obter a malha por grupo de recursos, nome do cofre e nome do tecido</span><span class="sxs-lookup"><span data-stu-id="311d1-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="311d1-113">Obter uma malha específica</span><span class="sxs-lookup"><span data-stu-id="311d1-113">Get a specific fabric</span></span>

## <span data-ttu-id="311d1-114">OS</span><span class="sxs-lookup"><span data-stu-id="311d1-114">PARAMETERS</span></span>

### <span data-ttu-id="311d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311d1-115">-DefaultProfile</span></span>
<span data-ttu-id="311d1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="311d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="311d1-117">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="311d1-117">-FabricName</span></span>
<span data-ttu-id="311d1-118">Nome do tecido.</span><span class="sxs-lookup"><span data-stu-id="311d1-118">Fabric name.</span></span>

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

### <span data-ttu-id="311d1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="311d1-119">-ResourceGroupName</span></span>
<span data-ttu-id="311d1-120">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="311d1-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="311d1-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="311d1-121">-ResourceName</span></span>
<span data-ttu-id="311d1-122">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="311d1-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="311d1-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="311d1-123">-SubscriptionId</span></span>
<span data-ttu-id="311d1-124">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="311d1-124">The subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="311d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311d1-125">CommonParameters</span></span>
<span data-ttu-id="311d1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="311d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311d1-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="311d1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311d1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="311d1-128">INPUTS</span></span>

## <span data-ttu-id="311d1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="311d1-129">OUTPUTS</span></span>

### <span data-ttu-id="311d1-130">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IFabric</span><span class="sxs-lookup"><span data-stu-id="311d1-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="311d1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="311d1-131">NOTES</span></span>

<span data-ttu-id="311d1-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="311d1-132">ALIASES</span></span>

## <span data-ttu-id="311d1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="311d1-133">RELATED LINKS</span></span>

