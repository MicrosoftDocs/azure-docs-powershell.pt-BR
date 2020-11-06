---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 66d8f15c58d1b4b92f19e23f5940ed7c8ba45d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599134"
---
# <span data-ttu-id="3d0d7-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d0d7-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="3d0d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d0d7-102">SYNOPSIS</span></span>
<span data-ttu-id="3d0d7-103">Cria uma nova configuração de migração e inicia a migração de entidades dos namespaces padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="3d0d7-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="3d0d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d0d7-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d0d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d0d7-105">DESCRIPTION</span></span>
<span data-ttu-id="3d0d7-106">O cmdlet **Start-AzServiceBusMigration** cria uma nova configuração de migração e inicia a migração de entidades dos namespaces padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="3d0d7-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="3d0d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d0d7-107">EXAMPLES</span></span>

### <span data-ttu-id="3d0d7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d0d7-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="3d0d7-109">Cria uma nova configuração de migração para os namespaces "TestingNamespaceStandardMirgation" para "TestingNamespacePremiumMirgation"</span><span class="sxs-lookup"><span data-stu-id="3d0d7-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="3d0d7-110">OS</span><span class="sxs-lookup"><span data-stu-id="3d0d7-110">PARAMETERS</span></span>

### <span data-ttu-id="3d0d7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d0d7-111">-AsJob</span></span>
<span data-ttu-id="3d0d7-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3d0d7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d0d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d0d7-113">-DefaultProfile</span></span>
<span data-ttu-id="3d0d7-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d0d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d0d7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d0d7-115">-Name</span></span>
<span data-ttu-id="3d0d7-116">Nome do namespace padrão</span><span class="sxs-lookup"><span data-stu-id="3d0d7-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="3d0d7-117">-Pré-migraçãoname</span><span class="sxs-lookup"><span data-stu-id="3d0d7-117">-PostMigrationName</span></span>
<span data-ttu-id="3d0d7-118">Nome pós-migração do namespace standrad na migração</span><span class="sxs-lookup"><span data-stu-id="3d0d7-118">Post Migration Name for Standrad Namespace in Migration</span></span>

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

### <span data-ttu-id="3d0d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d0d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="3d0d7-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3d0d7-120">Resource Group Name</span></span>

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

### <span data-ttu-id="3d0d7-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="3d0d7-121">-TargetNameSpace</span></span>
<span data-ttu-id="3d0d7-122">ID do braço do namespace Premium</span><span class="sxs-lookup"><span data-stu-id="3d0d7-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="3d0d7-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d0d7-123">-Confirm</span></span>
<span data-ttu-id="3d0d7-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d0d7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d0d7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d0d7-125">-WhatIf</span></span>
<span data-ttu-id="3d0d7-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d0d7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d0d7-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d0d7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d0d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d0d7-128">CommonParameters</span></span>
<span data-ttu-id="3d0d7-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d0d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d0d7-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d0d7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d0d7-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d0d7-131">INPUTS</span></span>

### <span data-ttu-id="3d0d7-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3d0d7-132">None</span></span>

## <span data-ttu-id="3d0d7-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d0d7-133">OUTPUTS</span></span>

### <span data-ttu-id="3d0d7-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3d0d7-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="3d0d7-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d0d7-135">NOTES</span></span>

## <span data-ttu-id="3d0d7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d0d7-136">RELATED LINKS</span></span>
