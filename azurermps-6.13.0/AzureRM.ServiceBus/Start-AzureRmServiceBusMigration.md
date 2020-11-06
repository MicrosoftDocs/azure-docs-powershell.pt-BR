---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/start-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
ms.openlocfilehash: 979db64fb11b4fffc901d96811b24be5c79f6b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430859"
---
# <span data-ttu-id="7f403-101">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="7f403-101">Start-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="7f403-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f403-102">SYNOPSIS</span></span>
<span data-ttu-id="7f403-103">Cria uma nova configuração de migração e inicia a migração de entidades dos namespaces padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="7f403-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f403-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f403-104">SYNTAX</span></span>

```
Start-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f403-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f403-105">DESCRIPTION</span></span>
<span data-ttu-id="7f403-106">O cmdlet **Start-AzureRmServiceBusMigration** cria uma nova configuração de migração e inicia a migração de entidades dos namespaces padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="7f403-106">The **Start-AzureRmServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="7f403-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f403-107">EXAMPLES</span></span>

### <span data-ttu-id="7f403-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7f403-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="7f403-109">Cria uma nova configuração de migração para os namespaces "TestingNamespaceStandardMirgation" para "TestingNamespacePremiumMirgation"</span><span class="sxs-lookup"><span data-stu-id="7f403-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="7f403-110">OS</span><span class="sxs-lookup"><span data-stu-id="7f403-110">PARAMETERS</span></span>

### <span data-ttu-id="7f403-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f403-111">-AsJob</span></span>
<span data-ttu-id="7f403-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7f403-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f403-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f403-113">-DefaultProfile</span></span>
<span data-ttu-id="7f403-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f403-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f403-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f403-115">-Name</span></span>
<span data-ttu-id="7f403-116">Nome do namespace padrão</span><span class="sxs-lookup"><span data-stu-id="7f403-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="7f403-117">-Pré-migraçãoname</span><span class="sxs-lookup"><span data-stu-id="7f403-117">-PostMigrationName</span></span>
<span data-ttu-id="7f403-118">Nome pós-migração do namespace standrad na migração</span><span class="sxs-lookup"><span data-stu-id="7f403-118">Post Migration Name for Standrad Namespace in Migration</span></span>

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

### <span data-ttu-id="7f403-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f403-119">-ResourceGroupName</span></span>
<span data-ttu-id="7f403-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7f403-120">Resource Group Name</span></span>

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

### <span data-ttu-id="7f403-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="7f403-121">-TargetNameSpace</span></span>
<span data-ttu-id="7f403-122">ID do braço do namespace Premium</span><span class="sxs-lookup"><span data-stu-id="7f403-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="7f403-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7f403-123">-Confirm</span></span>
<span data-ttu-id="7f403-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f403-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f403-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f403-125">-WhatIf</span></span>
<span data-ttu-id="7f403-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f403-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f403-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f403-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f403-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f403-128">CommonParameters</span></span>
<span data-ttu-id="7f403-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f403-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f403-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f403-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f403-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f403-131">INPUTS</span></span>

### <span data-ttu-id="7f403-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7f403-132">None</span></span>

## <span data-ttu-id="7f403-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f403-133">OUTPUTS</span></span>

### <span data-ttu-id="7f403-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="7f403-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="7f403-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f403-135">NOTES</span></span>

## <span data-ttu-id="7f403-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f403-136">RELATED LINKS</span></span>
