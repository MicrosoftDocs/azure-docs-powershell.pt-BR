---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 010e54b21d4abb3068f62e561c002fed6ca734d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890066"
---
# <span data-ttu-id="69116-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="69116-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="69116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69116-102">SYNOPSIS</span></span>
<span data-ttu-id="69116-103">Cria uma nova configuração de Migração e inicia a migração de entidades de namespaces Standard para Premium</span><span class="sxs-lookup"><span data-stu-id="69116-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="69116-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="69116-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69116-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="69116-105">DESCRIPTION</span></span>
<span data-ttu-id="69116-106">O cmdlet **Start-AzServiceBusMigration** cria uma nova configuração de Migração e inicia a migração de entidades de namespaces Standard para Premium</span><span class="sxs-lookup"><span data-stu-id="69116-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="69116-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69116-107">EXAMPLES</span></span>

### <span data-ttu-id="69116-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69116-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="69116-109">Cria uma nova configuração de migração para 'TestingNamespaceStandardMigration' para namespace 'TestingNamespacePremiumMigration' namespaces</span><span class="sxs-lookup"><span data-stu-id="69116-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="69116-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="69116-110">PARAMETERS</span></span>

### <span data-ttu-id="69116-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69116-111">-AsJob</span></span>
<span data-ttu-id="69116-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="69116-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69116-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69116-113">-DefaultProfile</span></span>
<span data-ttu-id="69116-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69116-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69116-115">-Name</span><span class="sxs-lookup"><span data-stu-id="69116-115">-Name</span></span>
<span data-ttu-id="69116-116">Nome do Namespace Padrão</span><span class="sxs-lookup"><span data-stu-id="69116-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69116-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="69116-117">-PostMigrationName</span></span>
<span data-ttu-id="69116-118">Post Migration Name for Standard Namespace in Migration</span><span class="sxs-lookup"><span data-stu-id="69116-118">Post Migration Name for Standard Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69116-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69116-119">-ResourceGroupName</span></span>
<span data-ttu-id="69116-120">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="69116-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69116-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="69116-121">-TargetNameSpace</span></span>
<span data-ttu-id="69116-122">Premium Namespace ARM Id</span><span class="sxs-lookup"><span data-stu-id="69116-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69116-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69116-123">-Confirm</span></span>
<span data-ttu-id="69116-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69116-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69116-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69116-125">-WhatIf</span></span>
<span data-ttu-id="69116-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69116-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69116-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69116-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69116-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69116-128">CommonParameters</span></span>
<span data-ttu-id="69116-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69116-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69116-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69116-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69116-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69116-131">INPUTS</span></span>

### <span data-ttu-id="69116-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="69116-132">None</span></span>

## <span data-ttu-id="69116-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="69116-133">OUTPUTS</span></span>

### <span data-ttu-id="69116-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="69116-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="69116-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="69116-135">NOTES</span></span>

## <span data-ttu-id="69116-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69116-136">RELATED LINKS</span></span>
