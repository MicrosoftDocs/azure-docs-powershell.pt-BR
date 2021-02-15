---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 6872eb3da4f67969dcb6ec57a9e300677bd4611b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114263"
---
# <span data-ttu-id="2e96e-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="2e96e-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="2e96e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e96e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e96e-103">Obtém os detalhes de uma malha de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e96e-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="2e96e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e96e-104">SYNTAX</span></span>

### <span data-ttu-id="2e96e-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2e96e-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e96e-106">Obter</span><span class="sxs-lookup"><span data-stu-id="2e96e-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2e96e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e96e-107">DESCRIPTION</span></span>
<span data-ttu-id="2e96e-108">Obtém os detalhes de uma malha de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e96e-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="2e96e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e96e-109">EXAMPLES</span></span>

### <span data-ttu-id="2e96e-110">Exemplo 1: Obter todas as malhas por grupo de recursos e nome do cofre</span><span class="sxs-lookup"><span data-stu-id="2e96e-110">Example 1: Get all fabrics by resource group and vault name</span></span>
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

<span data-ttu-id="2e96e-111">Obter todas as malhas no grupo de recursos e no cofre</span><span class="sxs-lookup"><span data-stu-id="2e96e-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="2e96e-112">Exemplo 2: Obter malha por grupo de recursos, nome do cofre e nome do malha</span><span class="sxs-lookup"><span data-stu-id="2e96e-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
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

<span data-ttu-id="2e96e-113">Obter uma malha específica</span><span class="sxs-lookup"><span data-stu-id="2e96e-113">Get a specific fabric</span></span>

## <span data-ttu-id="2e96e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e96e-114">PARAMETERS</span></span>

### <span data-ttu-id="2e96e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e96e-115">-DefaultProfile</span></span>
<span data-ttu-id="2e96e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e96e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e96e-117">-NomeDaArmásia</span><span class="sxs-lookup"><span data-stu-id="2e96e-117">-FabricName</span></span>
<span data-ttu-id="2e96e-118">Nome do malha.</span><span class="sxs-lookup"><span data-stu-id="2e96e-118">Fabric name.</span></span>

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

### <span data-ttu-id="2e96e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e96e-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e96e-120">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="2e96e-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="2e96e-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2e96e-121">-ResourceName</span></span>
<span data-ttu-id="2e96e-122">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e96e-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="2e96e-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e96e-123">-SubscriptionId</span></span>
<span data-ttu-id="2e96e-124">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="2e96e-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="2e96e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e96e-125">CommonParameters</span></span>
<span data-ttu-id="2e96e-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e96e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e96e-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e96e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e96e-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="2e96e-128">INPUTS</span></span>

## <span data-ttu-id="2e96e-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="2e96e-129">OUTPUTS</span></span>

### <span data-ttu-id="2e96e-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span><span class="sxs-lookup"><span data-stu-id="2e96e-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="2e96e-131">Notas</span><span class="sxs-lookup"><span data-stu-id="2e96e-131">NOTES</span></span>

<span data-ttu-id="2e96e-132">Aliases</span><span class="sxs-lookup"><span data-stu-id="2e96e-132">ALIASES</span></span>

## <span data-ttu-id="2e96e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e96e-133">RELATED LINKS</span></span>

