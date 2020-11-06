---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: 09e13e973178444496604843336c8f483508c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430317"
---
# <span data-ttu-id="be966-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="be966-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="be966-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be966-102">SYNOPSIS</span></span>
<span data-ttu-id="be966-103">Atualiza as propriedades de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="be966-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be966-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be966-104">SYNTAX</span></span>

### <span data-ttu-id="be966-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="be966-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be966-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="be966-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be966-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="be966-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be966-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be966-108">DESCRIPTION</span></span>
<span data-ttu-id="be966-109">O cmdlet **Update-AzureRmDataFactoryV2** atualiza as marcas ou as propriedades de identidade de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="be966-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="be966-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be966-110">EXAMPLES</span></span>

### <span data-ttu-id="be966-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="be966-111">Example 1</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

Confirm
Are you sure you want to update properties of the data factory 'WikiADF' in resource group 'ADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


DataFactoryName   : WikiADF
DataFactoryId     : /subscriptions/1e42591f-1f0c-4c5a-b7f2-a268f6105ec5/resourceGroups/adf/providers/Microsoft.DataF
                    actory/factories/wikiadf
ResourceGroupName : ADF
Location          : EastUS
Tags              : {[myNewTagName, myTagValue]}
Identity          :
ProvisioningState : Succeeded
```

<span data-ttu-id="be966-112">Esse comando atualiza as marcas do WikiADF de fábrica para um dicionário contendo uma marca chamada myNewTagName com o valor myTagValue.</span><span class="sxs-lookup"><span data-stu-id="be966-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="be966-113">OS</span><span class="sxs-lookup"><span data-stu-id="be966-113">PARAMETERS</span></span>

### <span data-ttu-id="be966-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be966-114">-DefaultProfile</span></span>
<span data-ttu-id="be966-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be966-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be966-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be966-116">-InputObject</span></span>
<span data-ttu-id="be966-117">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="be966-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be966-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="be966-118">-Name</span></span>
<span data-ttu-id="be966-119">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="be966-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be966-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be966-120">-ResourceGroupName</span></span>
<span data-ttu-id="be966-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="be966-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be966-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be966-122">-ResourceId</span></span>
<span data-ttu-id="be966-123">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="be966-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be966-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="be966-124">-Tag</span></span>
<span data-ttu-id="be966-125">As marcas do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="be966-125">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be966-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="be966-126">-Confirm</span></span>
<span data-ttu-id="be966-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be966-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be966-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be966-128">-WhatIf</span></span>
<span data-ttu-id="be966-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be966-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be966-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be966-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be966-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be966-131">CommonParameters</span></span>
<span data-ttu-id="be966-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be966-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be966-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be966-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be966-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be966-134">INPUTS</span></span>

### <span data-ttu-id="be966-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="be966-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="be966-136">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be966-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="be966-137">System. String</span><span class="sxs-lookup"><span data-stu-id="be966-137">System.String</span></span>

## <span data-ttu-id="be966-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be966-138">OUTPUTS</span></span>

### <span data-ttu-id="be966-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="be966-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="be966-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be966-140">NOTES</span></span>

## <span data-ttu-id="be966-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be966-141">RELATED LINKS</span></span>