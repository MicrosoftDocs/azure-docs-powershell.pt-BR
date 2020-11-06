---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a2515b3713f449d25963af5952e233117e078ba9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426730"
---
# <span data-ttu-id="e7a3c-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e7a3c-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e7a3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a3c-103">Remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7a3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7a3c-104">SYNTAX</span></span>

### <span data-ttu-id="e7a3c-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e7a3c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7a3c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a3c-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a3c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e7a3c-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a3c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7a3c-108">DESCRIPTION</span></span>
<span data-ttu-id="e7a3c-109">O cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="e7a3c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7a3c-110">EXAMPLES</span></span>

### <span data-ttu-id="e7a3c-111">Exemplo 1: remover um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="e7a3c-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="e7a3c-112">Esse comando Remove o tempo de execução de integração chamado "Test-reservou-ir" da fábrica de dados chamado "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="e7a3c-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="e7a3c-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="e7a3c-114">OS</span><span class="sxs-lookup"><span data-stu-id="e7a3c-114">PARAMETERS</span></span>

### <span data-ttu-id="e7a3c-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e7a3c-115">-DataFactoryName</span></span>
<span data-ttu-id="e7a3c-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a3c-117">-DefaultProfile</span></span>
<span data-ttu-id="e7a3c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e7a3c-119">-Force</span></span>
<span data-ttu-id="e7a3c-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7a3c-121">-InputObject</span></span>
<span data-ttu-id="e7a3c-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-122">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7a3c-123">-Name</span></span>
<span data-ttu-id="e7a3c-124">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-124">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a3c-125">-ResourceGroupName</span></span>
<span data-ttu-id="e7a3c-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a3c-127">-ResourceId</span></span>
<span data-ttu-id="e7a3c-128">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7a3c-129">-Confirm</span></span>
<span data-ttu-id="e7a3c-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a3c-131">-WhatIf</span></span>
<span data-ttu-id="e7a3c-132">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a3c-133">CommonParameters</span></span>
<span data-ttu-id="e7a3c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a3c-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7a3c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a3c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7a3c-136">INPUTS</span></span>

### <span data-ttu-id="e7a3c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e7a3c-137">System.String</span></span>
<span data-ttu-id="e7a3c-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e7a3c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e7a3c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7a3c-139">OUTPUTS</span></span>

### <span data-ttu-id="e7a3c-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="e7a3c-140">System.Object</span></span>

## <span data-ttu-id="e7a3c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7a3c-141">NOTES</span></span>
<span data-ttu-id="e7a3c-142">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="e7a3c-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="e7a3c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7a3c-143">RELATED LINKS</span></span>

[<span data-ttu-id="e7a3c-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e7a3c-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="e7a3c-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e7a3c-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

