---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: b351cfaa5d94c7104972158dc9dee6363a7d466b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889396"
---
# <span data-ttu-id="646bc-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="646bc-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="646bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="646bc-102">SYNOPSIS</span></span>
<span data-ttu-id="646bc-103">Exclui a configuração de espaço de trabalho de segurança para essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="646bc-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="646bc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="646bc-104">SYNTAX</span></span>

### <span data-ttu-id="646bc-105">SubscriptionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="646bc-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="646bc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="646bc-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="646bc-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="646bc-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="646bc-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="646bc-108">DESCRIPTION</span></span>
<span data-ttu-id="646bc-109">Exclui a configuração de espaço de trabalho de segurança para essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="646bc-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="646bc-110">Essa ação fará com que os agentes de segurança recém-instalados reportem ao espaço de trabalho padrão dessa assinatura.</span><span class="sxs-lookup"><span data-stu-id="646bc-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="646bc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="646bc-111">EXAMPLES</span></span>

### <span data-ttu-id="646bc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="646bc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="646bc-113">Exclui a configuração de espaço de trabalho de segurança para essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="646bc-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="646bc-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="646bc-114">PARAMETERS</span></span>

### <span data-ttu-id="646bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646bc-115">-DefaultProfile</span></span>
<span data-ttu-id="646bc-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="646bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="646bc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="646bc-117">-InputObject</span></span>
<span data-ttu-id="646bc-118">Objeto Input.</span><span class="sxs-lookup"><span data-stu-id="646bc-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="646bc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="646bc-119">-Name</span></span>
<span data-ttu-id="646bc-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="646bc-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646bc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="646bc-121">-PassThru</span></span>
<span data-ttu-id="646bc-122">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="646bc-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="646bc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="646bc-123">-ResourceId</span></span>
<span data-ttu-id="646bc-124">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="646bc-124">Resource ID.</span></span>

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

### <span data-ttu-id="646bc-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="646bc-125">-Confirm</span></span>
<span data-ttu-id="646bc-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="646bc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="646bc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="646bc-127">-WhatIf</span></span>
<span data-ttu-id="646bc-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="646bc-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="646bc-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="646bc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="646bc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646bc-130">CommonParameters</span></span>
<span data-ttu-id="646bc-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="646bc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646bc-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="646bc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646bc-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="646bc-133">INPUTS</span></span>

### <span data-ttu-id="646bc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="646bc-134">System.String</span></span>

### <span data-ttu-id="646bc-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="646bc-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="646bc-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="646bc-136">OUTPUTS</span></span>

### <span data-ttu-id="646bc-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="646bc-137">System.Boolean</span></span>

## <span data-ttu-id="646bc-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="646bc-138">NOTES</span></span>

## <span data-ttu-id="646bc-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="646bc-139">RELATED LINKS</span></span>
