---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 63ab8e9004b993429af31cb54e360c0b6d9854fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440189"
---
# <span data-ttu-id="22b79-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="22b79-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="22b79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22b79-102">SYNOPSIS</span></span>
<span data-ttu-id="22b79-103">Obtém definições de política.</span><span class="sxs-lookup"><span data-stu-id="22b79-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22b79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22b79-104">SYNTAX</span></span>

### <span data-ttu-id="22b79-105">O conjunto de parâmetros da lista todas as definições de política.</span><span class="sxs-lookup"><span data-stu-id="22b79-105">The list all policy definitions parameter set.</span></span> <span data-ttu-id="22b79-106">Assume</span><span class="sxs-lookup"><span data-stu-id="22b79-106">(Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22b79-107">O parâmetro nome da definição de política definido.</span><span class="sxs-lookup"><span data-stu-id="22b79-107">The policy definition name parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22b79-108">O conjunto de parâmetros de ID de definição de política.</span><span class="sxs-lookup"><span data-stu-id="22b79-108">The policy definition Id parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="22b79-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22b79-109">DESCRIPTION</span></span>
<span data-ttu-id="22b79-110">O cmdlet **Get-AzureRmPolicyDefinition** obtém todas as definições de política ou uma definição de política específica identificada por nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="22b79-110">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="22b79-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22b79-111">EXAMPLES</span></span>

### <span data-ttu-id="22b79-112">Exemplo 1: obter toda a definição da política</span><span class="sxs-lookup"><span data-stu-id="22b79-112">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="22b79-113">Esse comando obtém todas as definições de política.</span><span class="sxs-lookup"><span data-stu-id="22b79-113">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="22b79-114">Exemplo 2: obter a definição de política por nome</span><span class="sxs-lookup"><span data-stu-id="22b79-114">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="22b79-115">Esse comando obtém a definição de política chamada VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="22b79-115">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="22b79-116">OS</span><span class="sxs-lookup"><span data-stu-id="22b79-116">PARAMETERS</span></span>

### <span data-ttu-id="22b79-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22b79-117">-ApiVersion</span></span>
<span data-ttu-id="22b79-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="22b79-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="22b79-119">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="22b79-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="22b79-120">-ID</span><span class="sxs-lookup"><span data-stu-id="22b79-120">-Id</span></span>
<span data-ttu-id="22b79-121">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="22b79-121">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b79-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="22b79-122">-InformationAction</span></span>
<span data-ttu-id="22b79-123">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="22b79-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="22b79-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="22b79-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22b79-125">Contínuo</span><span class="sxs-lookup"><span data-stu-id="22b79-125">Continue</span></span>
- <span data-ttu-id="22b79-126">Ignorar</span><span class="sxs-lookup"><span data-stu-id="22b79-126">Ignore</span></span>
- <span data-ttu-id="22b79-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="22b79-127">Inquire</span></span>
- <span data-ttu-id="22b79-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="22b79-128">SilentlyContinue</span></span>
- <span data-ttu-id="22b79-129">Finaliza</span><span class="sxs-lookup"><span data-stu-id="22b79-129">Stop</span></span>
- <span data-ttu-id="22b79-130">Suspensão</span><span class="sxs-lookup"><span data-stu-id="22b79-130">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22b79-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="22b79-131">-InformationVariable</span></span>
<span data-ttu-id="22b79-132">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="22b79-132">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22b79-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="22b79-133">-Name</span></span>
<span data-ttu-id="22b79-134">Especifica o nome da definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="22b79-134">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b79-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="22b79-135">-Pre</span></span>
<span data-ttu-id="22b79-136">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="22b79-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="22b79-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b79-137">-DefaultProfile</span></span>
<span data-ttu-id="22b79-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22b79-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22b79-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b79-139">CommonParameters</span></span>
<span data-ttu-id="22b79-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b79-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b79-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b79-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b79-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22b79-142">INPUTS</span></span>

## <span data-ttu-id="22b79-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22b79-143">OUTPUTS</span></span>

### <span data-ttu-id="22b79-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="22b79-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="22b79-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22b79-145">NOTES</span></span>

## <span data-ttu-id="22b79-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22b79-146">RELATED LINKS</span></span>

[<span data-ttu-id="22b79-147">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="22b79-147">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="22b79-148">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="22b79-148">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="22b79-149">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="22b79-149">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


