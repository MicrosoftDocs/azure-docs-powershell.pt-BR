---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113273"
---
# <span data-ttu-id="643d7-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="643d7-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="643d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="643d7-102">SYNOPSIS</span></span>
<span data-ttu-id="643d7-103">Atualiza as propriedades de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="643d7-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="643d7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="643d7-104">SYNTAX</span></span>

### <span data-ttu-id="643d7-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="643d7-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="643d7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="643d7-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="643d7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="643d7-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="643d7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="643d7-108">DESCRIPTION</span></span>
<span data-ttu-id="643d7-109">O cmdlet **Update-AzDataFactoryV2** atualiza marcas ou propriedades de identidade de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="643d7-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="643d7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="643d7-110">EXAMPLES</span></span>

### <span data-ttu-id="643d7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="643d7-111">Example 1</span></span>
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

<span data-ttu-id="643d7-112">Este comando atualiza as marcas do WikiADF de fábrica para um dicionário que contém uma marca chamada myNewTagName com valor myTagValue.</span><span class="sxs-lookup"><span data-stu-id="643d7-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="643d7-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="643d7-113">PARAMETERS</span></span>

### <span data-ttu-id="643d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643d7-114">-DefaultProfile</span></span>
<span data-ttu-id="643d7-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="643d7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="643d7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="643d7-116">-InputObject</span></span>
<span data-ttu-id="643d7-117">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="643d7-117">The data factory object.</span></span>

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

### <span data-ttu-id="643d7-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="643d7-118">-Name</span></span>
<span data-ttu-id="643d7-119">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="643d7-119">The data factory name.</span></span>

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

### <span data-ttu-id="643d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="643d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="643d7-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="643d7-121">The resource group name.</span></span>

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

### <span data-ttu-id="643d7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="643d7-122">-ResourceId</span></span>
<span data-ttu-id="643d7-123">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="643d7-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="643d7-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="643d7-124">-Tag</span></span>
<span data-ttu-id="643d7-125">As marcas da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="643d7-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="643d7-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="643d7-126">-Confirm</span></span>
<span data-ttu-id="643d7-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="643d7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="643d7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="643d7-128">-WhatIf</span></span>
<span data-ttu-id="643d7-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="643d7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="643d7-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="643d7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="643d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643d7-131">CommonParameters</span></span>
<span data-ttu-id="643d7-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="643d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643d7-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="643d7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643d7-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="643d7-134">INPUTS</span></span>

### <span data-ttu-id="643d7-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="643d7-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="643d7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="643d7-136">System.String</span></span>

## <span data-ttu-id="643d7-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="643d7-137">OUTPUTS</span></span>

### <span data-ttu-id="643d7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="643d7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="643d7-139">Notas</span><span class="sxs-lookup"><span data-stu-id="643d7-139">NOTES</span></span>

## <span data-ttu-id="643d7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="643d7-140">RELATED LINKS</span></span>
