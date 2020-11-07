---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b0414b6fbbd4cdb0211b7dee1f85e172c1329c3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773257"
---
# <span data-ttu-id="4a6d0-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4a6d0-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="4a6d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6d0-103">Exclui uma política de acesso à rede JIT.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="4a6d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a6d0-104">SYNTAX</span></span>

### <span data-ttu-id="4a6d0-105">ResourceGroupLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="4a6d0-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6d0-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="4a6d0-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6d0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4a6d0-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a6d0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a6d0-108">DESCRIPTION</span></span>
<span data-ttu-id="4a6d0-109">Exclui uma política de acesso à rede just in time.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="4a6d0-110">Após essa ação, um usuário não poderá solicitar uma conexão de rede temporária nas VMs que foram configuradas dentro da política excluída.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="4a6d0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a6d0-111">EXAMPLES</span></span>

### <span data-ttu-id="4a6d0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a6d0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="4a6d0-113">Exclui uma política de acesso à rede just in time.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="4a6d0-114">OS</span><span class="sxs-lookup"><span data-stu-id="4a6d0-114">PARAMETERS</span></span>

### <span data-ttu-id="4a6d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6d0-115">-DefaultProfile</span></span>
<span data-ttu-id="4a6d0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a6d0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a6d0-117">-InputObject</span></span>
<span data-ttu-id="4a6d0-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-118">Input Object.</span></span>

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

### <span data-ttu-id="4a6d0-119">-Local</span><span class="sxs-lookup"><span data-stu-id="4a6d0-119">-Location</span></span>
<span data-ttu-id="4a6d0-120">Ponto.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-120">Location.</span></span>

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

### <span data-ttu-id="4a6d0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a6d0-121">-Name</span></span>
<span data-ttu-id="4a6d0-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-122">Resource name.</span></span>

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

### <span data-ttu-id="4a6d0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a6d0-123">-PassThru</span></span>
<span data-ttu-id="4a6d0-124">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="4a6d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a6d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a6d0-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-126">Resource group name.</span></span>

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

### <span data-ttu-id="4a6d0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a6d0-127">-ResourceId</span></span>
<span data-ttu-id="4a6d0-128">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-128">Resource ID.</span></span>

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

### <span data-ttu-id="4a6d0-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a6d0-129">-Confirm</span></span>
<span data-ttu-id="4a6d0-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a6d0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a6d0-131">-WhatIf</span></span>
<span data-ttu-id="4a6d0-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a6d0-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a6d0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6d0-134">CommonParameters</span></span>
<span data-ttu-id="4a6d0-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a6d0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6d0-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a6d0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6d0-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a6d0-137">INPUTS</span></span>

### <span data-ttu-id="4a6d0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4a6d0-138">System.String</span></span>

### <span data-ttu-id="4a6d0-139">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4a6d0-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="4a6d0-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a6d0-140">OUTPUTS</span></span>

### <span data-ttu-id="4a6d0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a6d0-141">System.Boolean</span></span>

## <span data-ttu-id="4a6d0-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a6d0-142">NOTES</span></span>

## <span data-ttu-id="4a6d0-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a6d0-143">RELATED LINKS</span></span>