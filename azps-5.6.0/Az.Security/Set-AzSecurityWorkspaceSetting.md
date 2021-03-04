---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 6bcee25399004d5fb8f485e9c58446713bedc5c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892368"
---
# <span data-ttu-id="7d099-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="7d099-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="7d099-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d099-102">SYNOPSIS</span></span>
<span data-ttu-id="7d099-103">Atualiza as configurações de espaço de trabalho da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7d099-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="7d099-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7d099-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d099-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7d099-105">DESCRIPTION</span></span>
<span data-ttu-id="7d099-106">Atualiza as configurações de espaço de trabalho da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7d099-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="7d099-107">O espaço de trabalho configurado manterá os dados de segurança coletados pelo agente agente do Azure Log Analytics instalado em VMs dentro dessa assinatura.</span><span class="sxs-lookup"><span data-stu-id="7d099-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="7d099-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d099-108">EXAMPLES</span></span>

### <span data-ttu-id="7d099-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d099-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="7d099-110">Define o espaço de trabalho "securityuserws" para manter todos os dados de segurança coletados pelo agente do Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="7d099-110">Sets the "securityuserws" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="7d099-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7d099-111">PARAMETERS</span></span>

### <span data-ttu-id="7d099-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d099-112">-DefaultProfile</span></span>
<span data-ttu-id="7d099-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d099-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d099-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7d099-114">-Name</span></span>
<span data-ttu-id="7d099-115">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7d099-115">Resource name.</span></span>

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

### <span data-ttu-id="7d099-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="7d099-116">-Scope</span></span>
<span data-ttu-id="7d099-117">Escopo.</span><span class="sxs-lookup"><span data-stu-id="7d099-117">Scope.</span></span>

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

### <span data-ttu-id="7d099-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7d099-118">-WorkspaceId</span></span>
<span data-ttu-id="7d099-119">ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d099-119">Workspace ID.</span></span>

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

### <span data-ttu-id="7d099-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d099-120">-Confirm</span></span>
<span data-ttu-id="7d099-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d099-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d099-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d099-122">-WhatIf</span></span>
<span data-ttu-id="7d099-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d099-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d099-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d099-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d099-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d099-125">CommonParameters</span></span>
<span data-ttu-id="7d099-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d099-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d099-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d099-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d099-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d099-128">INPUTS</span></span>

### <span data-ttu-id="7d099-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7d099-129">System.String</span></span>

## <span data-ttu-id="7d099-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7d099-130">OUTPUTS</span></span>

### <span data-ttu-id="7d099-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="7d099-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="7d099-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="7d099-132">NOTES</span></span>

## <span data-ttu-id="7d099-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d099-133">RELATED LINKS</span></span>
