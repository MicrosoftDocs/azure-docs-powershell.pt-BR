---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: ea36cf36b32df4c61c159e89cfdae12acdcc9509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431622"
---
# <span data-ttu-id="55f96-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="55f96-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="55f96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55f96-102">SYNOPSIS</span></span>
<span data-ttu-id="55f96-103">Cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="55f96-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55f96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55f96-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55f96-105">DESCRIPTION</span></span>
<span data-ttu-id="55f96-106">O cmdlet **New-AzureRmPolicySetDefinition** cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="55f96-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="55f96-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55f96-107">EXAMPLES</span></span>

### <span data-ttu-id="55f96-108">Exemplo 1: criar uma definição de conjunto de políticas usando um arquivo de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="55f96-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="55f96-109">Esse comando cria uma definição de conjunto de políticas chamada VMPolicyDefinition que contém as definições de política especificadas em C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="55f96-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="55f96-110">OS</span><span class="sxs-lookup"><span data-stu-id="55f96-110">PARAMETERS</span></span>

### <span data-ttu-id="55f96-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="55f96-111">-ApiVersion</span></span>
<span data-ttu-id="55f96-112">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="55f96-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="55f96-113">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="55f96-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="55f96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f96-114">-DefaultProfile</span></span>
<span data-ttu-id="55f96-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="55f96-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55f96-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="55f96-116">-Description</span></span>
<span data-ttu-id="55f96-117">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="55f96-117">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f96-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="55f96-118">-DisplayName</span></span>
<span data-ttu-id="55f96-119">O nome de exibição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="55f96-119">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f96-120">-Metadados</span><span class="sxs-lookup"><span data-stu-id="55f96-120">-Metadata</span></span>
<span data-ttu-id="55f96-121">Os metadados da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="55f96-121">The metadata for policy set definition.</span></span> <span data-ttu-id="55f96-122">Pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="55f96-122">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f96-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="55f96-123">-Name</span></span>
<span data-ttu-id="55f96-124">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="55f96-124">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f96-125">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="55f96-125">-Parameter</span></span>
<span data-ttu-id="55f96-126">A declaração Parameters para a definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="55f96-126">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="55f96-127">Isso pode ser um caminho para um nome de arquivo contendo a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="55f96-127">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f96-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="55f96-128">-PolicyDefinition</span></span>
<span data-ttu-id="55f96-129">Definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="55f96-129">The policy set definition.</span></span> <span data-ttu-id="55f96-130">Pode ser um caminho para um nome de arquivo que contenha as definições da política ou a definição do conjunto de políticas como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="55f96-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f96-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="55f96-131">-Pre</span></span>
<span data-ttu-id="55f96-132">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="55f96-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="55f96-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55f96-133">-Confirm</span></span>
<span data-ttu-id="55f96-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55f96-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f96-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f96-135">-WhatIf</span></span>
<span data-ttu-id="55f96-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55f96-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55f96-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55f96-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f96-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f96-138">CommonParameters</span></span>
<span data-ttu-id="55f96-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55f96-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f96-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55f96-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f96-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55f96-141">INPUTS</span></span>

### <span data-ttu-id="55f96-142">System. String</span><span class="sxs-lookup"><span data-stu-id="55f96-142">System.String</span></span>

## <span data-ttu-id="55f96-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55f96-143">OUTPUTS</span></span>

### <span data-ttu-id="55f96-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="55f96-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="55f96-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55f96-145">NOTES</span></span>

## <span data-ttu-id="55f96-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55f96-146">RELATED LINKS</span></span>
