---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 5140219c5392a7fb9c727998ae248d600edfde23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433020"
---
# <span data-ttu-id="fcfc4-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fcfc4-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="fcfc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcfc4-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfc4-103">Cria uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcfc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcfc4-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fcfc4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcfc4-105">DESCRIPTION</span></span>
<span data-ttu-id="fcfc4-106">O cmdlet **New-AzureRmPolicyDefinition** cria uma definição de política que inclui uma regra de política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="fcfc4-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="fcfc4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcfc4-107">EXAMPLES</span></span>

### <span data-ttu-id="fcfc4-108">Exemplo 1: criar uma definição de política usando um arquivo de política</span><span class="sxs-lookup"><span data-stu-id="fcfc4-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="fcfc4-109">Esse comando cria uma definição de política chamada VMPolicyDefinition que contém a regra de política especificada em C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="fcfc4-110">Exemplo 2: criar uma definição de política embutida</span><span class="sxs-lookup"><span data-stu-id="fcfc4-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="fcfc4-111">Esse comando cria uma definição de política chamada VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="fcfc4-112">O comando especifica a política como uma cadeia de caracteres em formato JSON válido.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="fcfc4-113">OS</span><span class="sxs-lookup"><span data-stu-id="fcfc4-113">PARAMETERS</span></span>

### <span data-ttu-id="fcfc4-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fcfc4-114">-ApiVersion</span></span>
<span data-ttu-id="fcfc4-115">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fcfc4-116">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fcfc4-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="fcfc4-117">-Description</span></span>
<span data-ttu-id="fcfc4-118">Especifica uma descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-118">Specifies a description for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfc4-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fcfc4-119">-DisplayName</span></span>
<span data-ttu-id="fcfc4-120">Especifica um nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-120">Specifies a display name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfc4-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fcfc4-121">-InformationAction</span></span>
<span data-ttu-id="fcfc4-122">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fcfc4-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fcfc4-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fcfc4-124">Contínuo</span><span class="sxs-lookup"><span data-stu-id="fcfc4-124">Continue</span></span>
- <span data-ttu-id="fcfc4-125">Ignorar</span><span class="sxs-lookup"><span data-stu-id="fcfc4-125">Ignore</span></span>
- <span data-ttu-id="fcfc4-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="fcfc4-126">Inquire</span></span>
- <span data-ttu-id="fcfc4-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fcfc4-127">SilentlyContinue</span></span>
- <span data-ttu-id="fcfc4-128">Finaliza</span><span class="sxs-lookup"><span data-stu-id="fcfc4-128">Stop</span></span>
- <span data-ttu-id="fcfc4-129">Suspensão</span><span class="sxs-lookup"><span data-stu-id="fcfc4-129">Suspend</span></span>

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

### <span data-ttu-id="fcfc4-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fcfc4-130">-InformationVariable</span></span>
<span data-ttu-id="fcfc4-131">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fcfc4-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcfc4-132">-Name</span></span>
<span data-ttu-id="fcfc4-133">Especifica um nome para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-133">Specifies a name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfc4-134">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="fcfc4-134">-Parameter</span></span>
<span data-ttu-id="fcfc4-135">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-135">The parameters declaration for policy definition.</span></span> <span data-ttu-id="fcfc4-136">Isso pode ser um caminho para um nome de arquivo contendo a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfc4-137">-Política</span><span class="sxs-lookup"><span data-stu-id="fcfc4-137">-Policy</span></span>
<span data-ttu-id="fcfc4-138">Especifica uma regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-138">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="fcfc4-139">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política em formato JSON.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-139">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfc4-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="fcfc4-140">-Pre</span></span>
<span data-ttu-id="fcfc4-141">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fcfc4-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfc4-142">-DefaultProfile</span></span>
<span data-ttu-id="fcfc4-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcfc4-144">-Metadados</span><span class="sxs-lookup"><span data-stu-id="fcfc4-144">-Metadata</span></span>
<span data-ttu-id="fcfc4-145">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-145">The metadata for policy definition.</span></span> <span data-ttu-id="fcfc4-146">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-146">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfc4-147">-Mode</span><span class="sxs-lookup"><span data-stu-id="fcfc4-147">-Mode</span></span>
<span data-ttu-id="fcfc4-148">O modo da definição de política.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-148">The mode of the policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfc4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfc4-149">CommonParameters</span></span>
<span data-ttu-id="fcfc4-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcfc4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfc4-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcfc4-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfc4-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcfc4-152">INPUTS</span></span>

## <span data-ttu-id="fcfc4-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcfc4-153">OUTPUTS</span></span>

### <span data-ttu-id="fcfc4-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fcfc4-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fcfc4-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcfc4-155">NOTES</span></span>

## <span data-ttu-id="fcfc4-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcfc4-156">RELATED LINKS</span></span>

[<span data-ttu-id="fcfc4-157">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fcfc4-157">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="fcfc4-158">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fcfc4-158">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="fcfc4-159">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fcfc4-159">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


