---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 9e53dab771486758cbd57c8f5c530a458df655d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885254"
---
# <span data-ttu-id="aa6dd-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="aa6dd-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="aa6dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="aa6dd-103">Cmdlet exclui a configuração de migração para namespaces Standard para Premium</span><span class="sxs-lookup"><span data-stu-id="aa6dd-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="aa6dd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aa6dd-104">SYNTAX</span></span>

### <span data-ttu-id="aa6dd-105">MigrationConfigurationPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aa6dd-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa6dd-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aa6dd-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa6dd-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa6dd-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa6dd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aa6dd-108">DESCRIPTION</span></span>
<span data-ttu-id="aa6dd-109">O cmdlet **Remove-AzServiceBusMigration** exclui a configuração de migração para namespaces Standard para Premium</span><span class="sxs-lookup"><span data-stu-id="aa6dd-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="aa6dd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa6dd-110">EXAMPLES</span></span>

### <span data-ttu-id="aa6dd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa6dd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="aa6dd-112">Exclui a configuração de migração 'TestingNamespaceStandardMigration'</span><span class="sxs-lookup"><span data-stu-id="aa6dd-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="aa6dd-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aa6dd-113">PARAMETERS</span></span>

### <span data-ttu-id="aa6dd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa6dd-114">-AsJob</span></span>
<span data-ttu-id="aa6dd-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="aa6dd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa6dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa6dd-116">-DefaultProfile</span></span>
<span data-ttu-id="aa6dd-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa6dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa6dd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa6dd-118">-InputObject</span></span>
<span data-ttu-id="aa6dd-119">Objeto Namespace Padrão de Migração de Barramento de Serviço</span><span class="sxs-lookup"><span data-stu-id="aa6dd-119">Service Bus Migration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa6dd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aa6dd-120">-Name</span></span>
<span data-ttu-id="aa6dd-121">Nome do Namespace Padrão</span><span class="sxs-lookup"><span data-stu-id="aa6dd-121">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa6dd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa6dd-122">-PassThru</span></span>
<span data-ttu-id="aa6dd-123">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="aa6dd-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="aa6dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa6dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa6dd-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="aa6dd-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa6dd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa6dd-126">-ResourceId</span></span>
<span data-ttu-id="aa6dd-127">ID de recurso namespace padrão de migração de barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="aa6dd-127">Service Bus Migration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa6dd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa6dd-128">-Confirm</span></span>
<span data-ttu-id="aa6dd-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa6dd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa6dd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa6dd-130">-WhatIf</span></span>
<span data-ttu-id="aa6dd-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa6dd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa6dd-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa6dd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa6dd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa6dd-133">CommonParameters</span></span>
<span data-ttu-id="aa6dd-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa6dd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa6dd-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa6dd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa6dd-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa6dd-136">INPUTS</span></span>

### <span data-ttu-id="aa6dd-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="aa6dd-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="aa6dd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="aa6dd-138">System.String</span></span>

## <span data-ttu-id="aa6dd-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aa6dd-139">OUTPUTS</span></span>

### <span data-ttu-id="aa6dd-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa6dd-140">System.Boolean</span></span>

## <span data-ttu-id="aa6dd-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="aa6dd-141">NOTES</span></span>

## <span data-ttu-id="aa6dd-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa6dd-142">RELATED LINKS</span></span>
