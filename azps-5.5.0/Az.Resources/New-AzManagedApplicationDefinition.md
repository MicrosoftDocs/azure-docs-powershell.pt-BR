---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113318"
---
# <span data-ttu-id="857f9-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="857f9-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="857f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="857f9-102">SYNOPSIS</span></span>
<span data-ttu-id="857f9-103">Cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="857f9-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="857f9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="857f9-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="857f9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="857f9-105">DESCRIPTION</span></span>
<span data-ttu-id="857f9-106">O **cmdlet New-AzManagedApplicationDefinition** cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="857f9-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="857f9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="857f9-107">EXAMPLES</span></span>

### <span data-ttu-id="857f9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="857f9-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="857f9-109">Esse comando cria uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="857f9-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="857f9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="857f9-110">PARAMETERS</span></span>

### <span data-ttu-id="857f9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="857f9-111">-ApiVersion</span></span>
<span data-ttu-id="857f9-112">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="857f9-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="857f9-113">Se não especificado, a versão da API será determinada automaticamente como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="857f9-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="857f9-114">-Autorização</span><span class="sxs-lookup"><span data-stu-id="857f9-114">-Authorization</span></span>
<span data-ttu-id="857f9-115">A autorização de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="857f9-115">The managed application definition authorization.</span></span>
<span data-ttu-id="857f9-116">Pares de autorização separados por vírgulas em um formato \<principalId\> de:\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="857f9-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857f9-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="857f9-117">-CreateUiDefinition</span></span>
<span data-ttu-id="857f9-118">A definição de aplicativo gerenciado criar definição de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="857f9-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="857f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857f9-119">-DefaultProfile</span></span>
<span data-ttu-id="857f9-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="857f9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="857f9-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="857f9-121">-Description</span></span>
<span data-ttu-id="857f9-122">A descrição da definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="857f9-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="857f9-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="857f9-123">-DisplayName</span></span>
<span data-ttu-id="857f9-124">O nome de exibição de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="857f9-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="857f9-125">-Local</span><span class="sxs-lookup"><span data-stu-id="857f9-125">-Location</span></span>
<span data-ttu-id="857f9-126">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="857f9-126">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857f9-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="857f9-127">-LockLevel</span></span>
<span data-ttu-id="857f9-128">O nível do bloqueio para definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="857f9-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857f9-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="857f9-129">-MainTemplate</span></span>
<span data-ttu-id="857f9-130">O modelo principal de definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="857f9-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="857f9-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="857f9-131">-Name</span></span>
<span data-ttu-id="857f9-132">O nome de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="857f9-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="857f9-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="857f9-133">-PackageFileUri</span></span>
<span data-ttu-id="857f9-134">O uri de arquivo de pacote de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="857f9-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="857f9-135">-Pré-</span><span class="sxs-lookup"><span data-stu-id="857f9-135">-Pre</span></span>
<span data-ttu-id="857f9-136">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="857f9-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="857f9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857f9-137">-ResourceGroupName</span></span>
<span data-ttu-id="857f9-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="857f9-138">The resource group name.</span></span>

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

### <span data-ttu-id="857f9-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="857f9-139">-Tag</span></span>
<span data-ttu-id="857f9-140">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="857f9-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="857f9-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="857f9-141">-Confirm</span></span>
<span data-ttu-id="857f9-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="857f9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="857f9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="857f9-143">-WhatIf</span></span>
<span data-ttu-id="857f9-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="857f9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="857f9-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="857f9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="857f9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857f9-146">CommonParameters</span></span>
<span data-ttu-id="857f9-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="857f9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857f9-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="857f9-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857f9-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="857f9-149">INPUTS</span></span>

### <span data-ttu-id="857f9-150">System.String</span><span class="sxs-lookup"><span data-stu-id="857f9-150">System.String</span></span>

### <span data-ttu-id="857f9-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="857f9-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="857f9-152">System.String[]</span><span class="sxs-lookup"><span data-stu-id="857f9-152">System.String[]</span></span>

### <span data-ttu-id="857f9-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="857f9-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="857f9-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="857f9-154">OUTPUTS</span></span>

### <span data-ttu-id="857f9-155">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="857f9-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="857f9-156">Notas</span><span class="sxs-lookup"><span data-stu-id="857f9-156">NOTES</span></span>

## <span data-ttu-id="857f9-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="857f9-157">RELATED LINKS</span></span>
