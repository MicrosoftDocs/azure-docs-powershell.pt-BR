---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: e706e9eb21f601ed1a266faa0afb888297f17fdb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114256"
---
# <span data-ttu-id="56bb9-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="56bb9-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="56bb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="56bb9-103">Obtém os detalhes do provedor de serviços de recuperação registrado.</span><span class="sxs-lookup"><span data-stu-id="56bb9-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="56bb9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56bb9-104">SYNTAX</span></span>

### <span data-ttu-id="56bb9-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="56bb9-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56bb9-106">Obter</span><span class="sxs-lookup"><span data-stu-id="56bb9-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="56bb9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="56bb9-107">DESCRIPTION</span></span>
<span data-ttu-id="56bb9-108">Obtém os detalhes do provedor de serviços de recuperação registrado.</span><span class="sxs-lookup"><span data-stu-id="56bb9-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="56bb9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="56bb9-109">EXAMPLES</span></span>

### <span data-ttu-id="56bb9-110">Exemplo 1: Obter todos os provedores no cofre</span><span class="sxs-lookup"><span data-stu-id="56bb9-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="56bb9-111">Listar tudo.</span><span class="sxs-lookup"><span data-stu-id="56bb9-111">List all.</span></span>

## <span data-ttu-id="56bb9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56bb9-112">PARAMETERS</span></span>

### <span data-ttu-id="56bb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bb9-113">-DefaultProfile</span></span>
<span data-ttu-id="56bb9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56bb9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56bb9-115">-NomeDaArmásia</span><span class="sxs-lookup"><span data-stu-id="56bb9-115">-FabricName</span></span>
<span data-ttu-id="56bb9-116">Nome do malha.</span><span class="sxs-lookup"><span data-stu-id="56bb9-116">Fabric name.</span></span>

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

### <span data-ttu-id="56bb9-117">-Nomedo Provedor</span><span class="sxs-lookup"><span data-stu-id="56bb9-117">-ProviderName</span></span>
<span data-ttu-id="56bb9-118">Nome do provedor de serviços de recuperação</span><span class="sxs-lookup"><span data-stu-id="56bb9-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="56bb9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56bb9-119">-ResourceGroupName</span></span>
<span data-ttu-id="56bb9-120">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="56bb9-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="56bb9-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="56bb9-121">-ResourceName</span></span>
<span data-ttu-id="56bb9-122">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="56bb9-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="56bb9-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56bb9-123">-SubscriptionId</span></span>
<span data-ttu-id="56bb9-124">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="56bb9-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="56bb9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bb9-125">CommonParameters</span></span>
<span data-ttu-id="56bb9-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56bb9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bb9-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56bb9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bb9-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="56bb9-128">INPUTS</span></span>

## <span data-ttu-id="56bb9-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="56bb9-129">OUTPUTS</span></span>

### <span data-ttu-id="56bb9-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="56bb9-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="56bb9-131">Notas</span><span class="sxs-lookup"><span data-stu-id="56bb9-131">NOTES</span></span>

<span data-ttu-id="56bb9-132">Aliases</span><span class="sxs-lookup"><span data-stu-id="56bb9-132">ALIASES</span></span>

## <span data-ttu-id="56bb9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56bb9-133">RELATED LINKS</span></span>

