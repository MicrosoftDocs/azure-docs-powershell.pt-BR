---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118659"
---
# <span data-ttu-id="db0c2-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="db0c2-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="db0c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="db0c2-103">Cria uma nova configuração de migração e inicia a migração de entidades de namespaces Padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="db0c2-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="db0c2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db0c2-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db0c2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="db0c2-105">DESCRIPTION</span></span>
<span data-ttu-id="db0c2-106">O **cmdlet Start-AzServiceBusMigration** cria uma nova configuração de migração e começa a migrar entidades de namespaces Padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="db0c2-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="db0c2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db0c2-107">EXAMPLES</span></span>

### <span data-ttu-id="db0c2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db0c2-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="db0c2-109">Cria uma nova configuração de migração para 'TestingNamespaceStandardMigration' para namespaces 'TestingNamespacePremiumMigration'</span><span class="sxs-lookup"><span data-stu-id="db0c2-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="db0c2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db0c2-110">PARAMETERS</span></span>

### <span data-ttu-id="db0c2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db0c2-111">-AsJob</span></span>
<span data-ttu-id="db0c2-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="db0c2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db0c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db0c2-113">-DefaultProfile</span></span>
<span data-ttu-id="db0c2-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db0c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db0c2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="db0c2-115">-Name</span></span>
<span data-ttu-id="db0c2-116">Nome do Namespace Padrão</span><span class="sxs-lookup"><span data-stu-id="db0c2-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="db0c2-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="db0c2-117">-PostMigrationName</span></span>
<span data-ttu-id="db0c2-118">Nome pós-migração para Namespace Padrão na Migração</span><span class="sxs-lookup"><span data-stu-id="db0c2-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="db0c2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db0c2-119">-ResourceGroupName</span></span>
<span data-ttu-id="db0c2-120">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="db0c2-120">Resource Group Name</span></span>

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

### <span data-ttu-id="db0c2-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="db0c2-121">-TargetNameSpace</span></span>
<span data-ttu-id="db0c2-122">Premium Namespace ARM Id</span><span class="sxs-lookup"><span data-stu-id="db0c2-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="db0c2-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="db0c2-123">-Confirm</span></span>
<span data-ttu-id="db0c2-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db0c2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db0c2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db0c2-125">-WhatIf</span></span>
<span data-ttu-id="db0c2-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="db0c2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db0c2-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db0c2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db0c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db0c2-128">CommonParameters</span></span>
<span data-ttu-id="db0c2-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db0c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db0c2-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db0c2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db0c2-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="db0c2-131">INPUTS</span></span>

### <span data-ttu-id="db0c2-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="db0c2-132">None</span></span>

## <span data-ttu-id="db0c2-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="db0c2-133">OUTPUTS</span></span>

### <span data-ttu-id="db0c2-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="db0c2-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="db0c2-135">Notas</span><span class="sxs-lookup"><span data-stu-id="db0c2-135">NOTES</span></span>

## <span data-ttu-id="db0c2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db0c2-136">RELATED LINKS</span></span>
