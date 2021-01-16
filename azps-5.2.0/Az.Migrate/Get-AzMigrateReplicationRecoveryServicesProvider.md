---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264045"
---
# <span data-ttu-id="0d271-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0d271-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="0d271-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d271-102">SYNOPSIS</span></span>
<span data-ttu-id="0d271-103">Obtém os detalhes do provedor de serviços de recuperação cadastrado.</span><span class="sxs-lookup"><span data-stu-id="0d271-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="0d271-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d271-104">SYNTAX</span></span>

### <span data-ttu-id="0d271-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="0d271-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d271-106">Obter</span><span class="sxs-lookup"><span data-stu-id="0d271-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d271-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d271-107">DESCRIPTION</span></span>
<span data-ttu-id="0d271-108">Obtém os detalhes do provedor de serviços de recuperação cadastrado.</span><span class="sxs-lookup"><span data-stu-id="0d271-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="0d271-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d271-109">EXAMPLES</span></span>

### <span data-ttu-id="0d271-110">Exemplo 1: obter todos os provedores no cofre</span><span class="sxs-lookup"><span data-stu-id="0d271-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="0d271-111">Listar tudo.</span><span class="sxs-lookup"><span data-stu-id="0d271-111">List all.</span></span>

## <span data-ttu-id="0d271-112">OS</span><span class="sxs-lookup"><span data-stu-id="0d271-112">PARAMETERS</span></span>

### <span data-ttu-id="0d271-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d271-113">-DefaultProfile</span></span>
<span data-ttu-id="0d271-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d271-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d271-115">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="0d271-115">-FabricName</span></span>
<span data-ttu-id="0d271-116">Nome do tecido.</span><span class="sxs-lookup"><span data-stu-id="0d271-116">Fabric name.</span></span>

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

### <span data-ttu-id="0d271-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="0d271-117">-ProviderName</span></span>
<span data-ttu-id="0d271-118">Nome do provedor de serviços de recuperação</span><span class="sxs-lookup"><span data-stu-id="0d271-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="0d271-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d271-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d271-120">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="0d271-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="0d271-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0d271-121">-ResourceName</span></span>
<span data-ttu-id="0d271-122">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="0d271-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="0d271-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d271-123">-SubscriptionId</span></span>
<span data-ttu-id="0d271-124">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="0d271-124">The subscription Id.</span></span>

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

### <span data-ttu-id="0d271-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d271-125">CommonParameters</span></span>
<span data-ttu-id="0d271-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d271-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d271-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d271-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d271-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d271-128">INPUTS</span></span>

## <span data-ttu-id="0d271-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d271-129">OUTPUTS</span></span>

### <span data-ttu-id="0d271-130">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0d271-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="0d271-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d271-131">NOTES</span></span>

<span data-ttu-id="0d271-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0d271-132">ALIASES</span></span>

## <span data-ttu-id="0d271-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d271-133">RELATED LINKS</span></span>

