---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 2b81a1983bb89af48115ead85c3392cc3d762734
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263798"
---
# <span data-ttu-id="e1af0-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="e1af0-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="e1af0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1af0-102">SYNOPSIS</span></span>
<span data-ttu-id="e1af0-103">Exclui a definição de registro.</span><span class="sxs-lookup"><span data-stu-id="e1af0-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="e1af0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1af0-104">SYNTAX</span></span>

### <span data-ttu-id="e1af0-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="e1af0-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1af0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e1af0-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1af0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1af0-107">DESCRIPTION</span></span>
<span data-ttu-id="e1af0-108">Exclui a definição de registro.</span><span class="sxs-lookup"><span data-stu-id="e1af0-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="e1af0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1af0-109">EXAMPLES</span></span>

### <span data-ttu-id="e1af0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e1af0-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="e1af0-111">Remove a definição de registro por nome no escopo padrão.</span><span class="sxs-lookup"><span data-stu-id="e1af0-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="e1af0-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e1af0-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="e1af0-113">Exclui a definição de registro fornecida ao objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="e1af0-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="e1af0-114">OS</span><span class="sxs-lookup"><span data-stu-id="e1af0-114">PARAMETERS</span></span>

### <span data-ttu-id="e1af0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1af0-115">-DefaultProfile</span></span>
<span data-ttu-id="e1af0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1af0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1af0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1af0-117">-InputObject</span></span>
<span data-ttu-id="e1af0-118">O objeto de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="e1af0-118">The registration definition object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1af0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1af0-119">-Name</span></span>
<span data-ttu-id="e1af0-120">O nome exclusivo da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="e1af0-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1af0-121">-Escopo</span><span class="sxs-lookup"><span data-stu-id="e1af0-121">-Scope</span></span>
<span data-ttu-id="e1af0-122">O escopo em que a definição de registro foi criada.</span><span class="sxs-lookup"><span data-stu-id="e1af0-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1af0-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1af0-123">-Confirm</span></span>
<span data-ttu-id="e1af0-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1af0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1af0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1af0-125">-WhatIf</span></span>
<span data-ttu-id="e1af0-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1af0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1af0-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1af0-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1af0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1af0-128">CommonParameters</span></span>
<span data-ttu-id="e1af0-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1af0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1af0-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1af0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1af0-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1af0-131">INPUTS</span></span>

### <span data-ttu-id="e1af0-132">Microsoft. Azure. PowerShell. cmdlets. Managedservices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="e1af0-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="e1af0-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1af0-133">OUTPUTS</span></span>

### <span data-ttu-id="e1af0-134">System. void</span><span class="sxs-lookup"><span data-stu-id="e1af0-134">System.Void</span></span>
## <span data-ttu-id="e1af0-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1af0-135">NOTES</span></span>

## <span data-ttu-id="e1af0-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1af0-136">RELATED LINKS</span></span>
