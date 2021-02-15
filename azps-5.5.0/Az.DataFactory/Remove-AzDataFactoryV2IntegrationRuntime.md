---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111964"
---
# <span data-ttu-id="190c1-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="190c1-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="190c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="190c1-102">SYNOPSIS</span></span>
<span data-ttu-id="190c1-103">Remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="190c1-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="190c1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="190c1-104">SYNTAX</span></span>

### <span data-ttu-id="190c1-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="190c1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190c1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="190c1-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190c1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="190c1-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="190c1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="190c1-108">DESCRIPTION</span></span>
<span data-ttu-id="190c1-109">O Remove-AzDataFactoryV2IntegrationRuntime cmdlet remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="190c1-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="190c1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="190c1-110">EXAMPLES</span></span>

### <span data-ttu-id="190c1-111">Exemplo 1: Remover um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="190c1-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="190c1-112">Esse comando remove o tempo de execução de integração chamado 'test-reserved-ir' da fábrica de dados chamada 'test-df'.</span><span class="sxs-lookup"><span data-stu-id="190c1-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="190c1-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="190c1-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="190c1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="190c1-114">PARAMETERS</span></span>

### <span data-ttu-id="190c1-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="190c1-115">-DataFactoryName</span></span>
<span data-ttu-id="190c1-116">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="190c1-116">The data factory name.</span></span>

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

### <span data-ttu-id="190c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190c1-117">-DefaultProfile</span></span>
<span data-ttu-id="190c1-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="190c1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="190c1-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="190c1-119">-Force</span></span>
<span data-ttu-id="190c1-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="190c1-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="190c1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="190c1-121">-InputObject</span></span>
<span data-ttu-id="190c1-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="190c1-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="190c1-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="190c1-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="190c1-124">O nome da fábrica de dados vinculada.</span><span class="sxs-lookup"><span data-stu-id="190c1-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="190c1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="190c1-125">-Name</span></span>
<span data-ttu-id="190c1-126">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="190c1-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="190c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="190c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="190c1-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="190c1-128">The resource group name.</span></span>

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

### <span data-ttu-id="190c1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="190c1-129">-ResourceId</span></span>
<span data-ttu-id="190c1-130">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="190c1-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="190c1-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="190c1-131">-Confirm</span></span>
<span data-ttu-id="190c1-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="190c1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="190c1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="190c1-133">-WhatIf</span></span>
<span data-ttu-id="190c1-134">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="190c1-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="190c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190c1-135">CommonParameters</span></span>
<span data-ttu-id="190c1-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="190c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190c1-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="190c1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190c1-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="190c1-138">INPUTS</span></span>

### <span data-ttu-id="190c1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="190c1-139">System.String</span></span>

### <span data-ttu-id="190c1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="190c1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="190c1-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="190c1-141">OUTPUTS</span></span>

### <span data-ttu-id="190c1-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="190c1-142">System.Void</span></span>

## <span data-ttu-id="190c1-143">Notas</span><span class="sxs-lookup"><span data-stu-id="190c1-143">NOTES</span></span>
<span data-ttu-id="190c1-144">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, keyword, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="190c1-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="190c1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="190c1-145">RELATED LINKS</span></span>

[<span data-ttu-id="190c1-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="190c1-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="190c1-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="190c1-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

