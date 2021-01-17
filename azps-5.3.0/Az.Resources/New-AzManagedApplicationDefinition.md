---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427269"
---
# <span data-ttu-id="faa26-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="faa26-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="faa26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="faa26-102">SYNOPSIS</span></span>
<span data-ttu-id="faa26-103">Cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="faa26-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="faa26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="faa26-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="faa26-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="faa26-105">DESCRIPTION</span></span>
<span data-ttu-id="faa26-106">O cmdlet **New-AzManagedApplicationDefinition** cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="faa26-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="faa26-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="faa26-107">EXAMPLES</span></span>

### <span data-ttu-id="faa26-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="faa26-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="faa26-109">Esse comando cria uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="faa26-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="faa26-110">OS</span><span class="sxs-lookup"><span data-stu-id="faa26-110">PARAMETERS</span></span>

### <span data-ttu-id="faa26-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="faa26-111">-ApiVersion</span></span>
<span data-ttu-id="faa26-112">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="faa26-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="faa26-113">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="faa26-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="faa26-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="faa26-114">-Authorization</span></span>
<span data-ttu-id="faa26-115">A autorização da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="faa26-115">The managed application definition authorization.</span></span>
<span data-ttu-id="faa26-116">Pares de autorização separados por vírgula em um formato de \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="faa26-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="faa26-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="faa26-117">-CreateUiDefinition</span></span>
<span data-ttu-id="faa26-118">A definição de aplicativo gerenciado criar definição da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="faa26-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="faa26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa26-119">-DefaultProfile</span></span>
<span data-ttu-id="faa26-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="faa26-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faa26-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="faa26-121">-Description</span></span>
<span data-ttu-id="faa26-122">A descrição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="faa26-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="faa26-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="faa26-123">-DisplayName</span></span>
<span data-ttu-id="faa26-124">O nome de exibição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="faa26-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="faa26-125">-Local</span><span class="sxs-lookup"><span data-stu-id="faa26-125">-Location</span></span>
<span data-ttu-id="faa26-126">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="faa26-126">The resource location.</span></span>

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

### <span data-ttu-id="faa26-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="faa26-127">-LockLevel</span></span>
<span data-ttu-id="faa26-128">O nível do bloqueio para a definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="faa26-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="faa26-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="faa26-129">-MainTemplate</span></span>
<span data-ttu-id="faa26-130">O modelo principal de definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="faa26-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="faa26-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="faa26-131">-Name</span></span>
<span data-ttu-id="faa26-132">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="faa26-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="faa26-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="faa26-133">-PackageFileUri</span></span>
<span data-ttu-id="faa26-134">O URI do arquivo do pacote de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="faa26-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="faa26-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="faa26-135">-Pre</span></span>
<span data-ttu-id="faa26-136">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="faa26-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="faa26-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa26-137">-ResourceGroupName</span></span>
<span data-ttu-id="faa26-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="faa26-138">The resource group name.</span></span>

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

### <span data-ttu-id="faa26-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="faa26-139">-Tag</span></span>
<span data-ttu-id="faa26-140">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="faa26-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="faa26-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="faa26-141">-Confirm</span></span>
<span data-ttu-id="faa26-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faa26-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa26-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa26-143">-WhatIf</span></span>
<span data-ttu-id="faa26-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="faa26-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faa26-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="faa26-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa26-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa26-146">CommonParameters</span></span>
<span data-ttu-id="faa26-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa26-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa26-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faa26-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa26-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="faa26-149">INPUTS</span></span>

### <span data-ttu-id="faa26-150">System. String</span><span class="sxs-lookup"><span data-stu-id="faa26-150">System.String</span></span>

### <span data-ttu-id="faa26-151">Microsoft. Azure. Commands. ResourceManager. cmdlets. Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="faa26-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="faa26-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="faa26-152">System.String[]</span></span>

### <span data-ttu-id="faa26-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="faa26-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="faa26-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="faa26-154">OUTPUTS</span></span>

### <span data-ttu-id="faa26-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="faa26-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="faa26-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="faa26-156">NOTES</span></span>

## <span data-ttu-id="faa26-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="faa26-157">RELATED LINKS</span></span>
