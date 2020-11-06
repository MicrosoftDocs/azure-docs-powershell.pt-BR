---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429346"
---
# <span data-ttu-id="ae030-101">Remove-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae030-101">Remove-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ae030-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae030-102">SYNOPSIS</span></span>
<span data-ttu-id="ae030-103">Exclui uma política de acesso à rede JIT.</span><span class="sxs-lookup"><span data-stu-id="ae030-103">Deletes a JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae030-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae030-104">SYNTAX</span></span>

### <span data-ttu-id="ae030-105">ResourceGroupLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae030-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae030-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="ae030-106">ResourceId</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae030-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae030-107">InputObject</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae030-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae030-108">DESCRIPTION</span></span>
<span data-ttu-id="ae030-109">Exclui uma política de acesso à rede just in time.</span><span class="sxs-lookup"><span data-stu-id="ae030-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="ae030-110">Após essa ação, um usuário não poderá solicitar uma conexão de rede temporária nas VMs que foram configuradas dentro da política excluída.</span><span class="sxs-lookup"><span data-stu-id="ae030-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="ae030-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae030-111">EXAMPLES</span></span>

### <span data-ttu-id="ae030-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae030-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="ae030-113">Exclui uma política de acesso à rede just in time.</span><span class="sxs-lookup"><span data-stu-id="ae030-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="ae030-114">OS</span><span class="sxs-lookup"><span data-stu-id="ae030-114">PARAMETERS</span></span>

### <span data-ttu-id="ae030-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae030-115">-DefaultProfile</span></span>
<span data-ttu-id="ae030-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae030-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae030-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae030-117">-InputObject</span></span>
<span data-ttu-id="ae030-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae030-118">Input Object.</span></span>

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae030-119">-Local</span><span class="sxs-lookup"><span data-stu-id="ae030-119">-Location</span></span>
<span data-ttu-id="ae030-120">Ponto.</span><span class="sxs-lookup"><span data-stu-id="ae030-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae030-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae030-121">-Name</span></span>
<span data-ttu-id="ae030-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ae030-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae030-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae030-123">-PassThru</span></span>
<span data-ttu-id="ae030-124">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ae030-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="ae030-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae030-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae030-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae030-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae030-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae030-127">-ResourceId</span></span>
<span data-ttu-id="ae030-128">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ae030-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae030-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae030-129">-Confirm</span></span>
<span data-ttu-id="ae030-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae030-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae030-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae030-131">-WhatIf</span></span>
<span data-ttu-id="ae030-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae030-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae030-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae030-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae030-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae030-134">CommonParameters</span></span>
<span data-ttu-id="ae030-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae030-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae030-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae030-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae030-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae030-137">INPUTS</span></span>

### <span data-ttu-id="ae030-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ae030-138">System.String</span></span>
<span data-ttu-id="ae030-139">Microsoft. Azure. Commands. Security. cmdlets. JitNetworkAccessPolicies. PSRemoveJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae030-139">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSRemoveJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ae030-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae030-140">OUTPUTS</span></span>

### <span data-ttu-id="ae030-141">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae030-141">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ae030-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae030-142">NOTES</span></span>

## <span data-ttu-id="ae030-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae030-143">RELATED LINKS</span></span>
