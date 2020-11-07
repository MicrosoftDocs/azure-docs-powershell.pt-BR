---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778260"
---
# <span data-ttu-id="47ead-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="47ead-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="47ead-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47ead-102">SYNOPSIS</span></span>
<span data-ttu-id="47ead-103">Atualiza as propriedades de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="47ead-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="47ead-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47ead-104">SYNTAX</span></span>

### <span data-ttu-id="47ead-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="47ead-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ead-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="47ead-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ead-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="47ead-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47ead-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47ead-108">DESCRIPTION</span></span>
<span data-ttu-id="47ead-109">O cmdlet **Update-AzDataFactoryV2** atualiza as marcas ou as propriedades de identidade de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="47ead-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="47ead-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47ead-110">EXAMPLES</span></span>

### <span data-ttu-id="47ead-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47ead-111">Example 1</span></span>
```
PS C:\> Update-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

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

<span data-ttu-id="47ead-112">Esse comando atualiza as marcas do WikiADF de fábrica para um dicionário contendo uma marca chamada myNewTagName com o valor myTagValue.</span><span class="sxs-lookup"><span data-stu-id="47ead-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="47ead-113">OS</span><span class="sxs-lookup"><span data-stu-id="47ead-113">PARAMETERS</span></span>

### <span data-ttu-id="47ead-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ead-114">-DefaultProfile</span></span>
<span data-ttu-id="47ead-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47ead-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47ead-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47ead-116">-InputObject</span></span>
<span data-ttu-id="47ead-117">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="47ead-117">The data factory object.</span></span>

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

### <span data-ttu-id="47ead-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="47ead-118">-Name</span></span>
<span data-ttu-id="47ead-119">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="47ead-119">The data factory name.</span></span>

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

### <span data-ttu-id="47ead-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47ead-120">-ResourceGroupName</span></span>
<span data-ttu-id="47ead-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="47ead-121">The resource group name.</span></span>

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

### <span data-ttu-id="47ead-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47ead-122">-ResourceId</span></span>
<span data-ttu-id="47ead-123">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="47ead-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="47ead-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="47ead-124">-Tag</span></span>
<span data-ttu-id="47ead-125">As marcas do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="47ead-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="47ead-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47ead-126">-Confirm</span></span>
<span data-ttu-id="47ead-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47ead-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ead-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ead-128">-WhatIf</span></span>
<span data-ttu-id="47ead-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47ead-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47ead-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47ead-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ead-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ead-131">CommonParameters</span></span>
<span data-ttu-id="47ead-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ead-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ead-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ead-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ead-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47ead-134">INPUTS</span></span>

### <span data-ttu-id="47ead-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="47ead-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="47ead-136">System. String</span><span class="sxs-lookup"><span data-stu-id="47ead-136">System.String</span></span>

## <span data-ttu-id="47ead-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47ead-137">OUTPUTS</span></span>

### <span data-ttu-id="47ead-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="47ead-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="47ead-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47ead-139">NOTES</span></span>

## <span data-ttu-id="47ead-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47ead-140">RELATED LINKS</span></span>
