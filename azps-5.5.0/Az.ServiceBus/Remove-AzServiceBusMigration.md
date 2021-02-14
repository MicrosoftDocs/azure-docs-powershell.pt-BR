---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117125"
---
# <span data-ttu-id="73f66-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="73f66-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="73f66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73f66-102">SYNOPSIS</span></span>
<span data-ttu-id="73f66-103">O Cmdlet exclui a configuração de migração dos namespaces Padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="73f66-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="73f66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73f66-104">SYNTAX</span></span>

### <span data-ttu-id="73f66-105">MigrationConfigurationPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="73f66-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f66-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="73f66-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f66-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73f66-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f66-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="73f66-108">DESCRIPTION</span></span>
<span data-ttu-id="73f66-109">O cmdlet **Remove-AzServiceBusMigration** exclui a configuração de migração dos namespaces Padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="73f66-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="73f66-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73f66-110">EXAMPLES</span></span>

### <span data-ttu-id="73f66-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73f66-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="73f66-112">Exclui a configuração de migração 'TestingNamespaceStandardMigration'</span><span class="sxs-lookup"><span data-stu-id="73f66-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="73f66-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73f66-113">PARAMETERS</span></span>

### <span data-ttu-id="73f66-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73f66-114">-AsJob</span></span>
<span data-ttu-id="73f66-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="73f66-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73f66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f66-116">-DefaultProfile</span></span>
<span data-ttu-id="73f66-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73f66-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f66-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73f66-118">-InputObject</span></span>
<span data-ttu-id="73f66-119">Objeto Namespace Padrão de Migração de Barra de Serviços</span><span class="sxs-lookup"><span data-stu-id="73f66-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="73f66-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="73f66-120">-Name</span></span>
<span data-ttu-id="73f66-121">Nome do Namespace Padrão</span><span class="sxs-lookup"><span data-stu-id="73f66-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="73f66-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73f66-122">-PassThru</span></span>
<span data-ttu-id="73f66-123">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="73f66-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="73f66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f66-124">-ResourceGroupName</span></span>
<span data-ttu-id="73f66-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="73f66-125">Resource Group Name</span></span>

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

### <span data-ttu-id="73f66-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f66-126">-ResourceId</span></span>
<span data-ttu-id="73f66-127">ID do Recurso Namespace Padrão de Migração de Barra de Serviços</span><span class="sxs-lookup"><span data-stu-id="73f66-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="73f66-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="73f66-128">-Confirm</span></span>
<span data-ttu-id="73f66-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73f66-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73f66-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f66-130">-WhatIf</span></span>
<span data-ttu-id="73f66-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="73f66-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73f66-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73f66-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73f66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f66-133">CommonParameters</span></span>
<span data-ttu-id="73f66-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f66-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f66-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f66-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="73f66-136">INPUTS</span></span>

### <span data-ttu-id="73f66-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="73f66-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="73f66-138">System.String</span><span class="sxs-lookup"><span data-stu-id="73f66-138">System.String</span></span>

## <span data-ttu-id="73f66-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="73f66-139">OUTPUTS</span></span>

### <span data-ttu-id="73f66-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73f66-140">System.Boolean</span></span>

## <span data-ttu-id="73f66-141">Notas</span><span class="sxs-lookup"><span data-stu-id="73f66-141">NOTES</span></span>

## <span data-ttu-id="73f66-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73f66-142">RELATED LINKS</span></span>
