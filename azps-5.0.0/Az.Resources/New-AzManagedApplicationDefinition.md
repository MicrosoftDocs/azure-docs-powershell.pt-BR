---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281622"
---
# <span data-ttu-id="148ed-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="148ed-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="148ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="148ed-102">SYNOPSIS</span></span>
<span data-ttu-id="148ed-103">Cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="148ed-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="148ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="148ed-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="148ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="148ed-105">DESCRIPTION</span></span>
<span data-ttu-id="148ed-106">O cmdlet **New-AzManagedApplicationDefinition** cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="148ed-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="148ed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="148ed-107">EXAMPLES</span></span>

### <span data-ttu-id="148ed-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="148ed-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="148ed-109">Esse comando cria uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="148ed-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="148ed-110">OS</span><span class="sxs-lookup"><span data-stu-id="148ed-110">PARAMETERS</span></span>

### <span data-ttu-id="148ed-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="148ed-111">-ApiVersion</span></span>
<span data-ttu-id="148ed-112">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="148ed-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="148ed-113">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="148ed-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="148ed-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="148ed-114">-Authorization</span></span>
<span data-ttu-id="148ed-115">A autorização da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="148ed-115">The managed application definition authorization.</span></span>
<span data-ttu-id="148ed-116">Pares de autorização separados por vírgula em um formato de \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="148ed-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="148ed-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="148ed-117">-CreateUiDefinition</span></span>
<span data-ttu-id="148ed-118">A definição de aplicativo gerenciado criar definição da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="148ed-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="148ed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="148ed-119">-DefaultProfile</span></span>
<span data-ttu-id="148ed-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="148ed-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="148ed-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="148ed-121">-Description</span></span>
<span data-ttu-id="148ed-122">A descrição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="148ed-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="148ed-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="148ed-123">-DisplayName</span></span>
<span data-ttu-id="148ed-124">O nome de exibição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="148ed-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="148ed-125">-Local</span><span class="sxs-lookup"><span data-stu-id="148ed-125">-Location</span></span>
<span data-ttu-id="148ed-126">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="148ed-126">The resource location.</span></span>

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

### <span data-ttu-id="148ed-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="148ed-127">-LockLevel</span></span>
<span data-ttu-id="148ed-128">O nível do bloqueio para a definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="148ed-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="148ed-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="148ed-129">-MainTemplate</span></span>
<span data-ttu-id="148ed-130">O modelo principal de definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="148ed-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="148ed-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="148ed-131">-Name</span></span>
<span data-ttu-id="148ed-132">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="148ed-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="148ed-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="148ed-133">-PackageFileUri</span></span>
<span data-ttu-id="148ed-134">O URI do arquivo do pacote de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="148ed-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="148ed-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="148ed-135">-Pre</span></span>
<span data-ttu-id="148ed-136">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="148ed-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="148ed-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="148ed-137">-ResourceGroupName</span></span>
<span data-ttu-id="148ed-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="148ed-138">The resource group name.</span></span>

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

### <span data-ttu-id="148ed-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="148ed-139">-Tag</span></span>
<span data-ttu-id="148ed-140">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="148ed-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="148ed-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="148ed-141">-Confirm</span></span>
<span data-ttu-id="148ed-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="148ed-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="148ed-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="148ed-143">-WhatIf</span></span>
<span data-ttu-id="148ed-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="148ed-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="148ed-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="148ed-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="148ed-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148ed-146">CommonParameters</span></span>
<span data-ttu-id="148ed-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="148ed-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148ed-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="148ed-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148ed-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="148ed-149">INPUTS</span></span>

### <span data-ttu-id="148ed-150">System. String</span><span class="sxs-lookup"><span data-stu-id="148ed-150">System.String</span></span>

### <span data-ttu-id="148ed-151">Microsoft. Azure. Commands. ResourceManager. cmdlets. Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="148ed-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="148ed-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="148ed-152">System.String[]</span></span>

### <span data-ttu-id="148ed-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="148ed-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="148ed-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="148ed-154">OUTPUTS</span></span>

### <span data-ttu-id="148ed-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="148ed-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="148ed-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="148ed-156">NOTES</span></span>

## <span data-ttu-id="148ed-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="148ed-157">RELATED LINKS</span></span>
