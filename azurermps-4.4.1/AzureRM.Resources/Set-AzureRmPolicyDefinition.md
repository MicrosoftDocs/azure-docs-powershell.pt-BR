---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 2404c0f2dc6c357503f23e7ed509f1c58c352c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610178"
---
# <span data-ttu-id="9c603-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9c603-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="9c603-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c603-102">SYNOPSIS</span></span>
<span data-ttu-id="9c603-103">Modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="9c603-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c603-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c603-104">SYNTAX</span></span>

### <span data-ttu-id="9c603-105">O parâmetro nome da definição de política definido.</span><span class="sxs-lookup"><span data-stu-id="9c603-105">The policy definition name parameter set.</span></span> <span data-ttu-id="9c603-106">Assume</span><span class="sxs-lookup"><span data-stu-id="9c603-106">(Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9c603-107">O conjunto de parâmetros de ID de definição de política.</span><span class="sxs-lookup"><span data-stu-id="9c603-107">The policy definition Id parameter set.</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9c603-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c603-108">DESCRIPTION</span></span>
<span data-ttu-id="9c603-109">O cmdlet **set-AzureRmPolicyDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="9c603-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="9c603-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c603-110">EXAMPLES</span></span>

### <span data-ttu-id="9c603-111">Exemplo 1: atualizar a descrição de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="9c603-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="9c603-112">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9c603-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="9c603-113">O comando armazena esse objeto na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9c603-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="9c603-114">O segundo comando atualiza a descrição da definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9c603-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="9c603-115">OS</span><span class="sxs-lookup"><span data-stu-id="9c603-115">PARAMETERS</span></span>

### <span data-ttu-id="9c603-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9c603-116">-ApiVersion</span></span>
<span data-ttu-id="9c603-117">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9c603-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9c603-118">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="9c603-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9c603-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9c603-119">-Description</span></span>
<span data-ttu-id="9c603-120">Especifica uma nova descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="9c603-120">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="9c603-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9c603-121">-DisplayName</span></span>
<span data-ttu-id="9c603-122">Especifica um novo nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="9c603-122">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="9c603-123">-ID</span><span class="sxs-lookup"><span data-stu-id="9c603-123">-Id</span></span>
<span data-ttu-id="9c603-124">Especifica a ID de recurso totalmente qualificado para a definição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9c603-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9c603-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9c603-125">-InformationAction</span></span>
<span data-ttu-id="9c603-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="9c603-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9c603-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9c603-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c603-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="9c603-128">Continue</span></span>
- <span data-ttu-id="9c603-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9c603-129">Ignore</span></span>
- <span data-ttu-id="9c603-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="9c603-130">Inquire</span></span>
- <span data-ttu-id="9c603-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9c603-131">SilentlyContinue</span></span>
- <span data-ttu-id="9c603-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="9c603-132">Stop</span></span>
- <span data-ttu-id="9c603-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="9c603-133">Suspend</span></span>

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

### <span data-ttu-id="9c603-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9c603-134">-InformationVariable</span></span>
<span data-ttu-id="9c603-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="9c603-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9c603-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c603-136">-Name</span></span>
<span data-ttu-id="9c603-137">Especifica o nome da definição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9c603-137">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9c603-138">-Política</span><span class="sxs-lookup"><span data-stu-id="9c603-138">-Policy</span></span>
<span data-ttu-id="9c603-139">Especifica a nova regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="9c603-139">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="9c603-140">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="9c603-140">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="9c603-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="9c603-141">-Pre</span></span>
<span data-ttu-id="9c603-142">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9c603-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9c603-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c603-143">-DefaultProfile</span></span>
<span data-ttu-id="9c603-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c603-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c603-145">-Metadados</span><span class="sxs-lookup"><span data-stu-id="9c603-145">-Metadata</span></span>
<span data-ttu-id="9c603-146">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="9c603-146">The metadata for policy definition.</span></span> <span data-ttu-id="9c603-147">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9c603-147">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="9c603-148">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c603-148">-Parameter</span></span>
<span data-ttu-id="9c603-149">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="9c603-149">The parameters declaration for policy definition.</span></span> <span data-ttu-id="9c603-150">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9c603-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="9c603-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c603-151">CommonParameters</span></span>
<span data-ttu-id="9c603-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c603-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c603-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c603-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c603-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c603-154">INPUTS</span></span>

## <span data-ttu-id="9c603-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c603-155">OUTPUTS</span></span>

### <span data-ttu-id="9c603-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9c603-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9c603-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c603-157">NOTES</span></span>

## <span data-ttu-id="9c603-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c603-158">RELATED LINKS</span></span>

[<span data-ttu-id="9c603-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9c603-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="9c603-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9c603-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="9c603-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9c603-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


