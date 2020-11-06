---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: d9d79374e426c6d895fbfcef957da20ed9721f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432911"
---
# <span data-ttu-id="09deb-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="09deb-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="09deb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09deb-102">SYNOPSIS</span></span>
<span data-ttu-id="09deb-103">Obtém definições de política.</span><span class="sxs-lookup"><span data-stu-id="09deb-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09deb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09deb-104">SYNTAX</span></span>

### <span data-ttu-id="09deb-105">GetAllPolicyDefinitions (padrão)</span><span class="sxs-lookup"><span data-stu-id="09deb-105">GetAllPolicyDefinitions (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="09deb-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="09deb-106">GetByPolicyDefintionName</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="09deb-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="09deb-107">GetByPolicyDefinitionId</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="09deb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09deb-108">DESCRIPTION</span></span>
<span data-ttu-id="09deb-109">O cmdlet **Get-AzureRmPolicyDefinition** obtém todas as definições de política ou uma definição de política específica identificada por nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="09deb-109">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="09deb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09deb-110">EXAMPLES</span></span>

### <span data-ttu-id="09deb-111">Exemplo 1: obter toda a definição da política</span><span class="sxs-lookup"><span data-stu-id="09deb-111">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="09deb-112">Esse comando obtém todas as definições de política.</span><span class="sxs-lookup"><span data-stu-id="09deb-112">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="09deb-113">Exemplo 2: obter a definição de política por nome</span><span class="sxs-lookup"><span data-stu-id="09deb-113">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="09deb-114">Esse comando obtém a definição de política chamada VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="09deb-114">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="09deb-115">OS</span><span class="sxs-lookup"><span data-stu-id="09deb-115">PARAMETERS</span></span>

### <span data-ttu-id="09deb-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="09deb-116">-ApiVersion</span></span>
<span data-ttu-id="09deb-117">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="09deb-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="09deb-118">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="09deb-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="09deb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09deb-119">-DefaultProfile</span></span>
<span data-ttu-id="09deb-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="09deb-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09deb-121">-ID</span><span class="sxs-lookup"><span data-stu-id="09deb-121">-Id</span></span>
<span data-ttu-id="09deb-122">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="09deb-122">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="09deb-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="09deb-123">-InformationAction</span></span>
<span data-ttu-id="09deb-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="09deb-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="09deb-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="09deb-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="09deb-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="09deb-126">Continue</span></span>
- <span data-ttu-id="09deb-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="09deb-127">Ignore</span></span>
- <span data-ttu-id="09deb-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="09deb-128">Inquire</span></span>
- <span data-ttu-id="09deb-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="09deb-129">SilentlyContinue</span></span>
- <span data-ttu-id="09deb-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="09deb-130">Stop</span></span>
- <span data-ttu-id="09deb-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="09deb-131">Suspend</span></span>

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

### <span data-ttu-id="09deb-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="09deb-132">-InformationVariable</span></span>
<span data-ttu-id="09deb-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="09deb-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="09deb-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="09deb-134">-Name</span></span>
<span data-ttu-id="09deb-135">Especifica o nome da definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="09deb-135">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="09deb-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="09deb-136">-Pre</span></span>
<span data-ttu-id="09deb-137">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="09deb-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="09deb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09deb-138">CommonParameters</span></span>
<span data-ttu-id="09deb-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09deb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09deb-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09deb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09deb-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09deb-141">INPUTS</span></span>

### <span data-ttu-id="09deb-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="09deb-142">None</span></span>
<span data-ttu-id="09deb-143">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="09deb-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09deb-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09deb-144">OUTPUTS</span></span>

### <span data-ttu-id="09deb-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="09deb-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="09deb-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09deb-146">NOTES</span></span>

## <span data-ttu-id="09deb-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09deb-147">RELATED LINKS</span></span>

[<span data-ttu-id="09deb-148">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="09deb-148">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="09deb-149">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="09deb-149">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="09deb-150">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="09deb-150">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


