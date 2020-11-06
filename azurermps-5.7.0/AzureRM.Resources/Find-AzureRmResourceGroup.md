---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 42e268a36cf6ea45d4a36ef1a7c3edd825c6e8ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431634"
---
# <span data-ttu-id="7a260-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7a260-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="7a260-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a260-102">SYNOPSIS</span></span>
<span data-ttu-id="7a260-103">Procura por grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a260-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a260-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a260-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a260-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a260-105">DESCRIPTION</span></span>
<span data-ttu-id="7a260-106">O cmdlet **Find-AzureRmResourceGroup** procura por grupos de recursos usando os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="7a260-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="7a260-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a260-107">EXAMPLES</span></span>

### <span data-ttu-id="7a260-108">Exemplo 1: localizar todos os grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="7a260-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="7a260-109">Esse comando localiza todos os grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a260-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="7a260-110">Exemplo 2: localizar grupos de recursos por nome da marca</span><span class="sxs-lookup"><span data-stu-id="7a260-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="7a260-111">Esse comando localiza todos os grupos de recursos que têm uma marca chamada testtag.</span><span class="sxs-lookup"><span data-stu-id="7a260-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="7a260-112">Exemplo 3: localizar grupos de recursos por nome e valor da marca</span><span class="sxs-lookup"><span data-stu-id="7a260-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="7a260-113">Esse comando localiza todos os grupos de recursos que têm uma marca chamada testtag e o valor testval.</span><span class="sxs-lookup"><span data-stu-id="7a260-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="7a260-114">OS</span><span class="sxs-lookup"><span data-stu-id="7a260-114">PARAMETERS</span></span>

### <span data-ttu-id="7a260-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7a260-115">-ApiVersion</span></span>
<span data-ttu-id="7a260-116">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7a260-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="7a260-117">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="7a260-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a260-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a260-118">-DefaultProfile</span></span>
<span data-ttu-id="7a260-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7a260-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a260-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="7a260-120">-Pre</span></span>
<span data-ttu-id="7a260-121">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="7a260-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7a260-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="7a260-122">-Tag</span></span>
<span data-ttu-id="7a260-123">Especifica as informações de marca como uma tabela de hash para filtrar seus resultados.</span><span class="sxs-lookup"><span data-stu-id="7a260-123">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="7a260-124">Use os seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="7a260-124">Use the following formats:</span></span>

<span data-ttu-id="7a260-125">@ {tagName = $null} ou @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="7a260-125">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a260-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a260-126">CommonParameters</span></span>
<span data-ttu-id="7a260-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a260-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a260-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a260-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a260-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a260-129">INPUTS</span></span>

### <span data-ttu-id="7a260-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7a260-130">None</span></span>
<span data-ttu-id="7a260-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7a260-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a260-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a260-132">OUTPUTS</span></span>

### <span data-ttu-id="7a260-133">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7a260-133">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7a260-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a260-134">NOTES</span></span>

## <span data-ttu-id="7a260-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a260-135">RELATED LINKS</span></span>
