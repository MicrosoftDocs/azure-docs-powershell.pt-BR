---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 423d79a1dddc95fb6d9437cbfc14d6157ccf8d90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118706"
---
# <span data-ttu-id="34b33-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34b33-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="34b33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34b33-102">SYNOPSIS</span></span>
<span data-ttu-id="34b33-103">Exclui uma política de acesso à rede JIT.</span><span class="sxs-lookup"><span data-stu-id="34b33-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="34b33-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34b33-104">SYNTAX</span></span>

### <span data-ttu-id="34b33-105">ResourceGroupLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="34b33-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34b33-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="34b33-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34b33-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="34b33-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34b33-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="34b33-108">DESCRIPTION</span></span>
<span data-ttu-id="34b33-109">Exclui uma política de acesso de rede Just In Time.</span><span class="sxs-lookup"><span data-stu-id="34b33-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="34b33-110">Após essa ação, um usuário não poderá solicitar conexão temporária de rede nos VMs que foram configurados dentro da política excluída.</span><span class="sxs-lookup"><span data-stu-id="34b33-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="34b33-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34b33-111">EXAMPLES</span></span>

### <span data-ttu-id="34b33-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34b33-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="34b33-113">Exclui uma política de acesso de rede Just In Time.</span><span class="sxs-lookup"><span data-stu-id="34b33-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="34b33-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34b33-114">PARAMETERS</span></span>

### <span data-ttu-id="34b33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b33-115">-DefaultProfile</span></span>
<span data-ttu-id="34b33-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34b33-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34b33-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34b33-117">-InputObject</span></span>
<span data-ttu-id="34b33-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="34b33-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34b33-119">-Local</span><span class="sxs-lookup"><span data-stu-id="34b33-119">-Location</span></span>
<span data-ttu-id="34b33-120">Localização.</span><span class="sxs-lookup"><span data-stu-id="34b33-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b33-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="34b33-121">-Name</span></span>
<span data-ttu-id="34b33-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="34b33-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b33-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34b33-123">-PassThru</span></span>
<span data-ttu-id="34b33-124">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="34b33-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="34b33-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b33-125">-ResourceGroupName</span></span>
<span data-ttu-id="34b33-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34b33-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b33-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34b33-127">-ResourceId</span></span>
<span data-ttu-id="34b33-128">A ID do recurso jit Network Access Policy.</span><span class="sxs-lookup"><span data-stu-id="34b33-128">The resource id of the jit Network Access Policy resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b33-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="34b33-129">-Confirm</span></span>
<span data-ttu-id="34b33-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34b33-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34b33-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34b33-131">-WhatIf</span></span>
<span data-ttu-id="34b33-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="34b33-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34b33-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34b33-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34b33-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b33-134">CommonParameters</span></span>
<span data-ttu-id="34b33-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34b33-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b33-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34b33-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b33-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="34b33-137">INPUTS</span></span>

### <span data-ttu-id="34b33-138">System.String</span><span class="sxs-lookup"><span data-stu-id="34b33-138">System.String</span></span>

### <span data-ttu-id="34b33-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34b33-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="34b33-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="34b33-140">OUTPUTS</span></span>

### <span data-ttu-id="34b33-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34b33-141">System.Boolean</span></span>

## <span data-ttu-id="34b33-142">Notas</span><span class="sxs-lookup"><span data-stu-id="34b33-142">NOTES</span></span>

## <span data-ttu-id="34b33-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34b33-143">RELATED LINKS</span></span>
