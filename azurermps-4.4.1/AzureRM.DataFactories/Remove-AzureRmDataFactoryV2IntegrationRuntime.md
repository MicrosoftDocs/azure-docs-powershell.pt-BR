---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: bf29e12292fba12cc6a5b4f99cef1e13f9d9fd8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431774"
---
# <span data-ttu-id="1f13b-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1f13b-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1f13b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f13b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f13b-103">Remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="1f13b-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f13b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f13b-104">SYNTAX</span></span>

### <span data-ttu-id="1f13b-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f13b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f13b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f13b-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f13b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1f13b-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f13b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f13b-108">DESCRIPTION</span></span>
<span data-ttu-id="1f13b-109">O cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="1f13b-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="1f13b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f13b-110">EXAMPLES</span></span>

### <span data-ttu-id="1f13b-111">Exemplo 1: remover um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="1f13b-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="1f13b-112">Esse comando Remove o tempo de execução de integração chamado "Test-reservou-ir" da fábrica de dados chamado "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="1f13b-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="1f13b-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="1f13b-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="1f13b-114">OS</span><span class="sxs-lookup"><span data-stu-id="1f13b-114">PARAMETERS</span></span>

### <span data-ttu-id="1f13b-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1f13b-115">-DataFactoryName</span></span>
<span data-ttu-id="1f13b-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="1f13b-116">The data factory name.</span></span>

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

### <span data-ttu-id="1f13b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1f13b-117">-Force</span></span>
<span data-ttu-id="1f13b-118">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="1f13b-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1f13b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f13b-119">-InputObject</span></span>
<span data-ttu-id="1f13b-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="1f13b-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="1f13b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f13b-121">-Name</span></span>
<span data-ttu-id="1f13b-122">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="1f13b-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="1f13b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f13b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f13b-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f13b-124">The resource group name.</span></span>

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

### <span data-ttu-id="1f13b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f13b-125">-ResourceId</span></span>
<span data-ttu-id="1f13b-126">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f13b-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1f13b-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f13b-127">-Confirm</span></span>
<span data-ttu-id="1f13b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f13b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f13b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f13b-129">-WhatIf</span></span>
<span data-ttu-id="1f13b-130">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f13b-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1f13b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f13b-131">-DefaultProfile</span></span>
<span data-ttu-id="1f13b-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f13b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f13b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f13b-133">CommonParameters</span></span>
<span data-ttu-id="1f13b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f13b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f13b-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f13b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f13b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f13b-136">INPUTS</span></span>

### <span data-ttu-id="1f13b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1f13b-137">System.String</span></span>
<span data-ttu-id="1f13b-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1f13b-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1f13b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f13b-139">OUTPUTS</span></span>

### <span data-ttu-id="1f13b-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="1f13b-140">System.Object</span></span>

## <span data-ttu-id="1f13b-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f13b-141">NOTES</span></span>
<span data-ttu-id="1f13b-142">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="1f13b-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="1f13b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f13b-143">RELATED LINKS</span></span>

[<span data-ttu-id="1f13b-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1f13b-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="1f13b-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1f13b-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

