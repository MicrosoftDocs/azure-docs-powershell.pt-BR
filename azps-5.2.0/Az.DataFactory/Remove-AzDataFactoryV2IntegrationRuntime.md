---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257606"
---
# <span data-ttu-id="7b486-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7b486-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="7b486-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b486-102">SYNOPSIS</span></span>
<span data-ttu-id="7b486-103">Remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="7b486-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="7b486-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b486-104">SYNTAX</span></span>

### <span data-ttu-id="7b486-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7b486-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b486-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b486-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b486-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7b486-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b486-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b486-108">DESCRIPTION</span></span>
<span data-ttu-id="7b486-109">O cmdlet Remove-AzDataFactoryV2IntegrationRuntime remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="7b486-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="7b486-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b486-110">EXAMPLES</span></span>

### <span data-ttu-id="7b486-111">Exemplo 1: remover um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="7b486-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="7b486-112">Esse comando Remove o tempo de execução de integração chamado "Test-reservou-ir" da fábrica de dados chamado "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="7b486-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="7b486-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="7b486-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="7b486-114">OS</span><span class="sxs-lookup"><span data-stu-id="7b486-114">PARAMETERS</span></span>

### <span data-ttu-id="7b486-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7b486-115">-DataFactoryName</span></span>
<span data-ttu-id="7b486-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="7b486-116">The data factory name.</span></span>

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

### <span data-ttu-id="7b486-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b486-117">-DefaultProfile</span></span>
<span data-ttu-id="7b486-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b486-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b486-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7b486-119">-Force</span></span>
<span data-ttu-id="7b486-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="7b486-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7b486-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b486-121">-InputObject</span></span>
<span data-ttu-id="7b486-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="7b486-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="7b486-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7b486-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="7b486-124">O nome do alocador de dados vinculado.</span><span class="sxs-lookup"><span data-stu-id="7b486-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="7b486-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b486-125">-Name</span></span>
<span data-ttu-id="7b486-126">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="7b486-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="7b486-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b486-127">-ResourceGroupName</span></span>
<span data-ttu-id="7b486-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7b486-128">The resource group name.</span></span>

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

### <span data-ttu-id="7b486-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b486-129">-ResourceId</span></span>
<span data-ttu-id="7b486-130">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b486-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7b486-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b486-131">-Confirm</span></span>
<span data-ttu-id="7b486-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b486-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b486-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b486-133">-WhatIf</span></span>
<span data-ttu-id="7b486-134">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b486-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7b486-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b486-135">CommonParameters</span></span>
<span data-ttu-id="7b486-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b486-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b486-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b486-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b486-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b486-138">INPUTS</span></span>

### <span data-ttu-id="7b486-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7b486-139">System.String</span></span>

### <span data-ttu-id="7b486-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7b486-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7b486-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b486-141">OUTPUTS</span></span>

### <span data-ttu-id="7b486-142">System. void</span><span class="sxs-lookup"><span data-stu-id="7b486-142">System.Void</span></span>

## <span data-ttu-id="7b486-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b486-143">NOTES</span></span>
<span data-ttu-id="7b486-144">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="7b486-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="7b486-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b486-145">RELATED LINKS</span></span>

[<span data-ttu-id="7b486-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7b486-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="7b486-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7b486-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

