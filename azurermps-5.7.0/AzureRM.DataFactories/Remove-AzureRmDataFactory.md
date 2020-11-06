---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 212e0c2ee4863c6d18873a717ff25f6940c34a15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428961"
---
# <span data-ttu-id="7da4b-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="7da4b-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="7da4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7da4b-102">SYNOPSIS</span></span>
<span data-ttu-id="7da4b-103">Remove uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="7da4b-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7da4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7da4b-104">SYNTAX</span></span>

### <span data-ttu-id="7da4b-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7da4b-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da4b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7da4b-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7da4b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7da4b-107">DESCRIPTION</span></span>
<span data-ttu-id="7da4b-108">O cmdlet **Remove-AzureRmDataFactory** remove uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="7da4b-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="7da4b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7da4b-109">EXAMPLES</span></span>

### <span data-ttu-id="7da4b-110">Exemplo 1: remover uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="7da4b-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="7da4b-111">Esse comando Remove a fábrica de dados chamada WikiADF do grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="7da4b-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="7da4b-112">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="7da4b-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="7da4b-113">OS</span><span class="sxs-lookup"><span data-stu-id="7da4b-113">PARAMETERS</span></span>

### <span data-ttu-id="7da4b-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="7da4b-114">-DataFactory</span></span>
<span data-ttu-id="7da4b-115">Especifica o objeto **PSDataFactory** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="7da4b-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="7da4b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da4b-116">-DefaultProfile</span></span>
<span data-ttu-id="7da4b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7da4b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7da4b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7da4b-118">-Force</span></span>
<span data-ttu-id="7da4b-119">Indica que esse cmdlet Remove uma fábrica de dados sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="7da4b-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7da4b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7da4b-120">-Name</span></span>
<span data-ttu-id="7da4b-121">Especifica o nome da fábrica de dados a ser removida.</span><span class="sxs-lookup"><span data-stu-id="7da4b-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da4b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da4b-122">-ResourceGroupName</span></span>
<span data-ttu-id="7da4b-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7da4b-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7da4b-124">Esse cmdlet Remove uma fábrica de dados do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7da4b-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7da4b-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7da4b-125">-Confirm</span></span>
<span data-ttu-id="7da4b-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7da4b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7da4b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da4b-127">-WhatIf</span></span>
<span data-ttu-id="7da4b-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7da4b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7da4b-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7da4b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7da4b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da4b-130">CommonParameters</span></span>
<span data-ttu-id="7da4b-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da4b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da4b-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da4b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da4b-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7da4b-133">INPUTS</span></span>

### <span data-ttu-id="7da4b-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7da4b-134">None</span></span>
<span data-ttu-id="7da4b-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7da4b-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7da4b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7da4b-136">OUTPUTS</span></span>

### <span data-ttu-id="7da4b-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7da4b-137">System.Boolean</span></span>

## <span data-ttu-id="7da4b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7da4b-138">NOTES</span></span>
* <span data-ttu-id="7da4b-139">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="7da4b-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7da4b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7da4b-140">RELATED LINKS</span></span>

[<span data-ttu-id="7da4b-141">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="7da4b-141">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="7da4b-142">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="7da4b-142">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


