---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 25106d6facb65346360bf7c78b7cbef27fc9a517
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889253"
---
# <span data-ttu-id="11acf-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="11acf-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="11acf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11acf-102">SYNOPSIS</span></span>
<span data-ttu-id="11acf-103">Obtém os detalhes de uma malha de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="11acf-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="11acf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="11acf-104">SYNTAX</span></span>

### <span data-ttu-id="11acf-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="11acf-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11acf-106">Obter</span><span class="sxs-lookup"><span data-stu-id="11acf-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="11acf-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="11acf-107">DESCRIPTION</span></span>
<span data-ttu-id="11acf-108">Obtém os detalhes de uma malha de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="11acf-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="11acf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11acf-109">EXAMPLES</span></span>

### <span data-ttu-id="11acf-110">Exemplo 1: Obter todos os malhas por grupo de recursos e nome do cofre</span><span class="sxs-lookup"><span data-stu-id="11acf-110">Example 1: Get all fabrics by resource group and vault name</span></span>
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

<span data-ttu-id="11acf-111">Obter todos os malhas no grupo de recursos e no cofre</span><span class="sxs-lookup"><span data-stu-id="11acf-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="11acf-112">Exemplo 2: Obter malha por grupo de recursos, nome do cofre e nome de malha</span><span class="sxs-lookup"><span data-stu-id="11acf-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
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

<span data-ttu-id="11acf-113">Obter uma malha específica</span><span class="sxs-lookup"><span data-stu-id="11acf-113">Get a specific fabric</span></span>

## <span data-ttu-id="11acf-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="11acf-114">PARAMETERS</span></span>

### <span data-ttu-id="11acf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11acf-115">-DefaultProfile</span></span>
<span data-ttu-id="11acf-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11acf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11acf-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="11acf-117">-FabricName</span></span>
<span data-ttu-id="11acf-118">Nome do fabric.</span><span class="sxs-lookup"><span data-stu-id="11acf-118">Fabric name.</span></span>

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

### <span data-ttu-id="11acf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11acf-119">-ResourceGroupName</span></span>
<span data-ttu-id="11acf-120">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="11acf-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="11acf-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="11acf-121">-ResourceName</span></span>
<span data-ttu-id="11acf-122">O nome do cofre dos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="11acf-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="11acf-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11acf-123">-SubscriptionId</span></span>
<span data-ttu-id="11acf-124">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="11acf-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="11acf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11acf-125">CommonParameters</span></span>
<span data-ttu-id="11acf-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11acf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11acf-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11acf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11acf-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11acf-128">INPUTS</span></span>

## <span data-ttu-id="11acf-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="11acf-129">OUTPUTS</span></span>

### <span data-ttu-id="11acf-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span><span class="sxs-lookup"><span data-stu-id="11acf-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="11acf-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="11acf-131">NOTES</span></span>

<span data-ttu-id="11acf-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="11acf-132">ALIASES</span></span>

## <span data-ttu-id="11acf-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11acf-133">RELATED LINKS</span></span>

