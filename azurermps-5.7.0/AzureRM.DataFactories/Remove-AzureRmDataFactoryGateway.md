---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: b781207bae8b967acadf4a9ef3ae50c5ffc9cfef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430507"
---
# <span data-ttu-id="38b95-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="38b95-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="38b95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38b95-102">SYNOPSIS</span></span>
<span data-ttu-id="38b95-103">Remove um gateway do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="38b95-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38b95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38b95-104">SYNTAX</span></span>

### <span data-ttu-id="38b95-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="38b95-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38b95-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="38b95-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38b95-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38b95-107">DESCRIPTION</span></span>
<span data-ttu-id="38b95-108">O cmdlet **Remove-AzureRmDataFactoryGateway** remove o gateway especificado do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="38b95-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="38b95-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38b95-109">EXAMPLES</span></span>

### <span data-ttu-id="38b95-110">Exemplo 1: remover um gateway</span><span class="sxs-lookup"><span data-stu-id="38b95-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="38b95-111">Esse comando Remove o gateway chamado ContosoGateway da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="38b95-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="38b95-112">OS</span><span class="sxs-lookup"><span data-stu-id="38b95-112">PARAMETERS</span></span>

### <span data-ttu-id="38b95-113">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="38b95-113">-DataFactory</span></span>
<span data-ttu-id="38b95-114">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="38b95-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="38b95-115">Esse cmdlet Remove um gateway da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="38b95-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b95-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="38b95-116">-DataFactoryName</span></span>
<span data-ttu-id="38b95-117">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="38b95-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="38b95-118">Esse cmdlet Remove um gateway da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="38b95-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b95-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b95-119">-DefaultProfile</span></span>
<span data-ttu-id="38b95-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="38b95-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38b95-121">-Force</span><span class="sxs-lookup"><span data-stu-id="38b95-121">-Force</span></span>
<span data-ttu-id="38b95-122">Indica que esse cmdlet Remove um gateway sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="38b95-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="38b95-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="38b95-123">-Name</span></span>
<span data-ttu-id="38b95-124">Especifica o nome do gateway a ser removido.</span><span class="sxs-lookup"><span data-stu-id="38b95-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b95-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b95-125">-ResourceGroupName</span></span>
<span data-ttu-id="38b95-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="38b95-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="38b95-127">Esse cmdlet Remove um gateway que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="38b95-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b95-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38b95-128">-Confirm</span></span>
<span data-ttu-id="38b95-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38b95-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b95-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b95-130">-WhatIf</span></span>
<span data-ttu-id="38b95-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38b95-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38b95-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38b95-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b95-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b95-133">CommonParameters</span></span>
<span data-ttu-id="38b95-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b95-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b95-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b95-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b95-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38b95-136">INPUTS</span></span>

### <span data-ttu-id="38b95-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="38b95-137">None</span></span>
<span data-ttu-id="38b95-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="38b95-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38b95-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38b95-139">OUTPUTS</span></span>

### <span data-ttu-id="38b95-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38b95-140">System.Boolean</span></span>

## <span data-ttu-id="38b95-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38b95-141">NOTES</span></span>
* <span data-ttu-id="38b95-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="38b95-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="38b95-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38b95-143">RELATED LINKS</span></span>

[<span data-ttu-id="38b95-144">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="38b95-144">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="38b95-145">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="38b95-145">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="38b95-146">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="38b95-146">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


