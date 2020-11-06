---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: d7e01294836145b09844fa3bca49421df20f67d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432902"
---
# <span data-ttu-id="04b46-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="04b46-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="04b46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04b46-102">SYNOPSIS</span></span>
<span data-ttu-id="04b46-103">Modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="04b46-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04b46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04b46-104">SYNTAX</span></span>

### <span data-ttu-id="04b46-105">SetByPolicyDefinitionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="04b46-105">SetByPolicyDefinitionName (Default)</span></span>
```
Set-AzureRmPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="04b46-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="04b46-106">GetByPolicyDefintionName</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="04b46-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="04b46-107">GetByPolicyDefinitionId</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="04b46-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04b46-108">DESCRIPTION</span></span>
<span data-ttu-id="04b46-109">O cmdlet **set-AzureRmPolicyDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="04b46-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="04b46-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04b46-110">EXAMPLES</span></span>

### <span data-ttu-id="04b46-111">Exemplo 1: atualizar a descrição de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="04b46-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="04b46-112">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="04b46-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="04b46-113">O comando armazena esse objeto na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="04b46-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="04b46-114">O segundo comando atualiza a descrição da definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="04b46-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="04b46-115">OS</span><span class="sxs-lookup"><span data-stu-id="04b46-115">PARAMETERS</span></span>

### <span data-ttu-id="04b46-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="04b46-116">-ApiVersion</span></span>
<span data-ttu-id="04b46-117">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="04b46-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="04b46-118">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="04b46-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="04b46-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b46-119">-DefaultProfile</span></span>
<span data-ttu-id="04b46-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="04b46-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04b46-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="04b46-121">-Description</span></span>
<span data-ttu-id="04b46-122">Especifica uma nova descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="04b46-122">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="04b46-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="04b46-123">-DisplayName</span></span>
<span data-ttu-id="04b46-124">Especifica um novo nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="04b46-124">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="04b46-125">-ID</span><span class="sxs-lookup"><span data-stu-id="04b46-125">-Id</span></span>
<span data-ttu-id="04b46-126">Especifica a ID de recurso totalmente qualificado para a definição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="04b46-126">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04b46-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="04b46-127">-InformationAction</span></span>
<span data-ttu-id="04b46-128">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="04b46-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="04b46-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="04b46-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04b46-130">Contínuo</span><span class="sxs-lookup"><span data-stu-id="04b46-130">Continue</span></span>
- <span data-ttu-id="04b46-131">Ignorar</span><span class="sxs-lookup"><span data-stu-id="04b46-131">Ignore</span></span>
- <span data-ttu-id="04b46-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="04b46-132">Inquire</span></span>
- <span data-ttu-id="04b46-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="04b46-133">SilentlyContinue</span></span>
- <span data-ttu-id="04b46-134">Finaliza</span><span class="sxs-lookup"><span data-stu-id="04b46-134">Stop</span></span>
- <span data-ttu-id="04b46-135">Suspensão</span><span class="sxs-lookup"><span data-stu-id="04b46-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b46-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="04b46-136">-InformationVariable</span></span>
<span data-ttu-id="04b46-137">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="04b46-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b46-138">-Metadados</span><span class="sxs-lookup"><span data-stu-id="04b46-138">-Metadata</span></span>
<span data-ttu-id="04b46-139">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="04b46-139">The metadata for policy definition.</span></span> <span data-ttu-id="04b46-140">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="04b46-140">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="04b46-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="04b46-141">-Name</span></span>
<span data-ttu-id="04b46-142">Especifica o nome da definição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="04b46-142">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04b46-143">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="04b46-143">-Parameter</span></span>
<span data-ttu-id="04b46-144">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="04b46-144">The parameters declaration for policy definition.</span></span> <span data-ttu-id="04b46-145">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="04b46-145">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="04b46-146">-Política</span><span class="sxs-lookup"><span data-stu-id="04b46-146">-Policy</span></span>
<span data-ttu-id="04b46-147">Especifica a nova regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="04b46-147">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="04b46-148">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="04b46-148">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="04b46-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="04b46-149">-Pre</span></span>
<span data-ttu-id="04b46-150">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="04b46-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="04b46-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b46-151">CommonParameters</span></span>
<span data-ttu-id="04b46-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b46-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b46-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04b46-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b46-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04b46-154">INPUTS</span></span>

### <span data-ttu-id="04b46-155">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="04b46-155">None</span></span>
<span data-ttu-id="04b46-156">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="04b46-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04b46-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04b46-157">OUTPUTS</span></span>

### <span data-ttu-id="04b46-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="04b46-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="04b46-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04b46-159">NOTES</span></span>

## <span data-ttu-id="04b46-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04b46-160">RELATED LINKS</span></span>

[<span data-ttu-id="04b46-161">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="04b46-161">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="04b46-162">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="04b46-162">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="04b46-163">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="04b46-163">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


