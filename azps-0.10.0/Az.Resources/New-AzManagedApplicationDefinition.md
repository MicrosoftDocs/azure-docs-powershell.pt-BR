---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: 286dcf7812f3ca796c8d2049112aa2cc64f96bd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776399"
---
# <span data-ttu-id="11301-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="11301-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="11301-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11301-102">SYNOPSIS</span></span>
<span data-ttu-id="11301-103">Cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11301-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="11301-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11301-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11301-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11301-105">DESCRIPTION</span></span>
<span data-ttu-id="11301-106">O cmdlet **New-AzManagedApplicationDefinition** cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11301-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="11301-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11301-107">EXAMPLES</span></span>

### <span data-ttu-id="11301-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11301-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="11301-109">Esse comando cria uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="11301-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="11301-110">OS</span><span class="sxs-lookup"><span data-stu-id="11301-110">PARAMETERS</span></span>

### <span data-ttu-id="11301-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="11301-111">-ApiVersion</span></span>
<span data-ttu-id="11301-112">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="11301-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="11301-113">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="11301-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="11301-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="11301-114">-Authorization</span></span>
<span data-ttu-id="11301-115">A autorização da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11301-115">The managed application definition authorization.</span></span>
<span data-ttu-id="11301-116">Pares de autorização separados por vírgula em um formato de \< Principado \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="11301-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="11301-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="11301-117">-CreateUiDefinition</span></span>
<span data-ttu-id="11301-118">A definição de aplicativo gerenciado criar definição da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="11301-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="11301-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11301-119">-DefaultProfile</span></span>
<span data-ttu-id="11301-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11301-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11301-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="11301-121">-Description</span></span>
<span data-ttu-id="11301-122">A descrição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11301-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="11301-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="11301-123">-DisplayName</span></span>
<span data-ttu-id="11301-124">O nome de exibição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11301-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="11301-125">-Local</span><span class="sxs-lookup"><span data-stu-id="11301-125">-Location</span></span>
<span data-ttu-id="11301-126">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="11301-126">The resource location.</span></span>

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

### <span data-ttu-id="11301-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="11301-127">-LockLevel</span></span>
<span data-ttu-id="11301-128">O nível do bloqueio para a definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11301-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="11301-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="11301-129">-MainTemplate</span></span>
<span data-ttu-id="11301-130">O modelo principal de definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="11301-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="11301-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="11301-131">-Name</span></span>
<span data-ttu-id="11301-132">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11301-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="11301-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="11301-133">-PackageFileUri</span></span>
<span data-ttu-id="11301-134">O URI do arquivo do pacote de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11301-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="11301-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="11301-135">-Pre</span></span>
<span data-ttu-id="11301-136">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="11301-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="11301-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11301-137">-ResourceGroupName</span></span>
<span data-ttu-id="11301-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11301-138">The resource group name.</span></span>

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

### <span data-ttu-id="11301-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="11301-139">-Tag</span></span>
<span data-ttu-id="11301-140">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="11301-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="11301-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11301-141">-Confirm</span></span>
<span data-ttu-id="11301-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11301-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11301-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11301-143">-WhatIf</span></span>
<span data-ttu-id="11301-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11301-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11301-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11301-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11301-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11301-146">CommonParameters</span></span>
<span data-ttu-id="11301-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11301-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11301-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11301-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11301-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11301-149">INPUTS</span></span>

### <span data-ttu-id="11301-150">System. String</span><span class="sxs-lookup"><span data-stu-id="11301-150">System.String</span></span>

### <span data-ttu-id="11301-151">Microsoft. Azure. Commands. ResourceManager. cmdlets. Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="11301-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="11301-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="11301-152">System.String[]</span></span>

### <span data-ttu-id="11301-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="11301-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="11301-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11301-154">OUTPUTS</span></span>

### <span data-ttu-id="11301-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="11301-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="11301-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11301-156">NOTES</span></span>

## <span data-ttu-id="11301-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11301-157">RELATED LINKS</span></span>
