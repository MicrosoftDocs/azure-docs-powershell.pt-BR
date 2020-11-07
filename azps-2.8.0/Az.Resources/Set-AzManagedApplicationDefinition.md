---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: d1da0ce7f8a88a12b0714960a60d5b2aa523a0a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773307"
---
# <span data-ttu-id="76a2a-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="76a2a-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="76a2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="76a2a-103">Atualiza a definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="76a2a-103">Updates managed application definition</span></span>

## <span data-ttu-id="76a2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76a2a-104">SYNTAX</span></span>

### <span data-ttu-id="76a2a-105">SetByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="76a2a-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76a2a-106">SetById</span><span class="sxs-lookup"><span data-stu-id="76a2a-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a2a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76a2a-107">DESCRIPTION</span></span>
<span data-ttu-id="76a2a-108">O cmdlet **set-AzManagedApplicationDefinition** atualiza as definições do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="76a2a-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="76a2a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76a2a-109">EXAMPLES</span></span>

### <span data-ttu-id="76a2a-110">Exemplo 1: atualizar descrição da definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="76a2a-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="76a2a-111">Este comando atualiza a descrição da definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="76a2a-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="76a2a-112">OS</span><span class="sxs-lookup"><span data-stu-id="76a2a-112">PARAMETERS</span></span>

### <span data-ttu-id="76a2a-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="76a2a-113">-ApiVersion</span></span>
<span data-ttu-id="76a2a-114">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="76a2a-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="76a2a-115">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="76a2a-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="76a2a-116">-Authorization</span><span class="sxs-lookup"><span data-stu-id="76a2a-116">-Authorization</span></span>
<span data-ttu-id="76a2a-117">A autorização da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="76a2a-117">The managed application definition authorization.</span></span>
<span data-ttu-id="76a2a-118">Pares de autorização separados por vírgula em um formato de \< Principado \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="76a2a-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a2a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a2a-119">-DefaultProfile</span></span>
<span data-ttu-id="76a2a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76a2a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76a2a-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="76a2a-121">-Description</span></span>
<span data-ttu-id="76a2a-122">A descrição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="76a2a-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="76a2a-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="76a2a-123">-DisplayName</span></span>
<span data-ttu-id="76a2a-124">O nome de exibição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="76a2a-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="76a2a-125">-ID</span><span class="sxs-lookup"><span data-stu-id="76a2a-125">-Id</span></span>
<span data-ttu-id="76a2a-126">A ID da definição do aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="76a2a-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="76a2a-127">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a2a-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a2a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="76a2a-128">-Name</span></span>
<span data-ttu-id="76a2a-129">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="76a2a-129">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a2a-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="76a2a-130">-PackageFileUri</span></span>
<span data-ttu-id="76a2a-131">O URI do arquivo do pacote de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="76a2a-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="76a2a-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="76a2a-132">-Pre</span></span>
<span data-ttu-id="76a2a-133">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="76a2a-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="76a2a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a2a-134">-ResourceGroupName</span></span>
<span data-ttu-id="76a2a-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76a2a-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a2a-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="76a2a-136">-Tag</span></span>
<span data-ttu-id="76a2a-137">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="76a2a-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a2a-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76a2a-138">-Confirm</span></span>
<span data-ttu-id="76a2a-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76a2a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76a2a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a2a-140">-WhatIf</span></span>
<span data-ttu-id="76a2a-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76a2a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a2a-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76a2a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76a2a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a2a-143">CommonParameters</span></span>
<span data-ttu-id="76a2a-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a2a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a2a-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76a2a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a2a-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76a2a-146">INPUTS</span></span>

### <span data-ttu-id="76a2a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="76a2a-147">System.String</span></span>

### <span data-ttu-id="76a2a-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="76a2a-148">System.String[]</span></span>

### <span data-ttu-id="76a2a-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="76a2a-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="76a2a-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76a2a-150">OUTPUTS</span></span>

### <span data-ttu-id="76a2a-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="76a2a-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="76a2a-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76a2a-152">NOTES</span></span>

## <span data-ttu-id="76a2a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76a2a-153">RELATED LINKS</span></span>