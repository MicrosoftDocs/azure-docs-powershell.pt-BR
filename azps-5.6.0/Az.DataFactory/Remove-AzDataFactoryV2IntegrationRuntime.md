---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 72b00b855bcc50df2766a6b8d0315780aaa64ecf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892860"
---
# <span data-ttu-id="b4039-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b4039-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="b4039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4039-102">SYNOPSIS</span></span>
<span data-ttu-id="b4039-103">Remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b4039-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="b4039-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b4039-104">SYNTAX</span></span>

### <span data-ttu-id="b4039-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b4039-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4039-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4039-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4039-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b4039-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4039-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b4039-108">DESCRIPTION</span></span>
<span data-ttu-id="b4039-109">O Remove-AzDataFactoryV2IntegrationRuntime cmdlet remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b4039-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="b4039-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4039-110">EXAMPLES</span></span>

### <span data-ttu-id="b4039-111">Exemplo 1: Remover um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="b4039-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="b4039-112">Este comando remove o tempo de execução de integração chamado 'test-reserved-ir' do fábrica de dados chamado 'test-df'.</span><span class="sxs-lookup"><span data-stu-id="b4039-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="b4039-113">Este comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="b4039-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="b4039-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b4039-114">PARAMETERS</span></span>

### <span data-ttu-id="b4039-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b4039-115">-DataFactoryName</span></span>
<span data-ttu-id="b4039-116">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b4039-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4039-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4039-117">-DefaultProfile</span></span>
<span data-ttu-id="b4039-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b4039-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4039-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b4039-119">-Force</span></span>
<span data-ttu-id="b4039-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="b4039-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b4039-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4039-121">-InputObject</span></span>
<span data-ttu-id="b4039-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b4039-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4039-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b4039-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="b4039-124">O nome da fábrica de dados vinculados.</span><span class="sxs-lookup"><span data-stu-id="b4039-124">The linked data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4039-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b4039-125">-Name</span></span>
<span data-ttu-id="b4039-126">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b4039-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4039-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4039-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4039-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4039-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4039-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4039-129">-ResourceId</span></span>
<span data-ttu-id="b4039-130">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4039-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4039-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4039-131">-Confirm</span></span>
<span data-ttu-id="b4039-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4039-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4039-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4039-133">-WhatIf</span></span>
<span data-ttu-id="b4039-134">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4039-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b4039-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4039-135">CommonParameters</span></span>
<span data-ttu-id="b4039-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4039-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4039-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4039-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4039-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4039-138">INPUTS</span></span>

### <span data-ttu-id="b4039-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b4039-139">System.String</span></span>

### <span data-ttu-id="b4039-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b4039-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b4039-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b4039-141">OUTPUTS</span></span>

### <span data-ttu-id="b4039-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="b4039-142">System.Void</span></span>

## <span data-ttu-id="b4039-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="b4039-143">NOTES</span></span>
<span data-ttu-id="b4039-144">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="b4039-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="b4039-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4039-145">RELATED LINKS</span></span>

[<span data-ttu-id="b4039-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b4039-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="b4039-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b4039-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

