---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: 2e890de56cdcf0ac2b17853b10629a58fce6c3b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889240"
---
# <span data-ttu-id="502fb-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="502fb-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="502fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="502fb-102">SYNOPSIS</span></span>
<span data-ttu-id="502fb-103">Obtém os detalhes do provedor de serviços de recuperação registrado.</span><span class="sxs-lookup"><span data-stu-id="502fb-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="502fb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="502fb-104">SYNTAX</span></span>

### <span data-ttu-id="502fb-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="502fb-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="502fb-106">Obter</span><span class="sxs-lookup"><span data-stu-id="502fb-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="502fb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="502fb-107">DESCRIPTION</span></span>
<span data-ttu-id="502fb-108">Obtém os detalhes do provedor de serviços de recuperação registrado.</span><span class="sxs-lookup"><span data-stu-id="502fb-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="502fb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="502fb-109">EXAMPLES</span></span>

### <span data-ttu-id="502fb-110">Exemplo 1: Obter todos os provedores no cofre</span><span class="sxs-lookup"><span data-stu-id="502fb-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="502fb-111">Listar tudo.</span><span class="sxs-lookup"><span data-stu-id="502fb-111">List all.</span></span>

## <span data-ttu-id="502fb-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="502fb-112">PARAMETERS</span></span>

### <span data-ttu-id="502fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502fb-113">-DefaultProfile</span></span>
<span data-ttu-id="502fb-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="502fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="502fb-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="502fb-115">-FabricName</span></span>
<span data-ttu-id="502fb-116">Nome do fabric.</span><span class="sxs-lookup"><span data-stu-id="502fb-116">Fabric name.</span></span>

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

### <span data-ttu-id="502fb-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="502fb-117">-ProviderName</span></span>
<span data-ttu-id="502fb-118">Nome do provedor de serviços de recuperação</span><span class="sxs-lookup"><span data-stu-id="502fb-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="502fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="502fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="502fb-120">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="502fb-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="502fb-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="502fb-121">-ResourceName</span></span>
<span data-ttu-id="502fb-122">O nome do cofre dos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="502fb-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="502fb-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="502fb-123">-SubscriptionId</span></span>
<span data-ttu-id="502fb-124">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="502fb-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="502fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502fb-125">CommonParameters</span></span>
<span data-ttu-id="502fb-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="502fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502fb-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="502fb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502fb-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="502fb-128">INPUTS</span></span>

## <span data-ttu-id="502fb-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="502fb-129">OUTPUTS</span></span>

### <span data-ttu-id="502fb-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="502fb-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="502fb-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="502fb-131">NOTES</span></span>

<span data-ttu-id="502fb-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="502fb-132">ALIASES</span></span>

## <span data-ttu-id="502fb-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="502fb-133">RELATED LINKS</span></span>

