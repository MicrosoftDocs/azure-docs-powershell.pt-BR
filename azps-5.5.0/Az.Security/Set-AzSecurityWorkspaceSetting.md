---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: a02d2685987844db5f88fafaf12d0c9aed4a3234
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117164"
---
# <span data-ttu-id="4f379-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="4f379-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="4f379-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f379-102">SYNOPSIS</span></span>
<span data-ttu-id="4f379-103">Atualiza as configurações de espaço de trabalho da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4f379-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="4f379-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f379-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f379-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f379-105">DESCRIPTION</span></span>
<span data-ttu-id="4f379-106">Atualiza as configurações de espaço de trabalho da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4f379-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="4f379-107">O espaço de trabalho configurado conterá os dados de segurança que foram coletados pelo agente do Azure Log Analytics que está instalado em VMs dentro desta assinatura.</span><span class="sxs-lookup"><span data-stu-id="4f379-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="4f379-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f379-108">EXAMPLES</span></span>

### <span data-ttu-id="4f379-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f379-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="4f379-110">Define o espaço de trabalho "securityuserws" para manter todos os dados de segurança coletados pelo agente de Análise de Log do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f379-110">Sets the "securityuserws" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="4f379-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f379-111">PARAMETERS</span></span>

### <span data-ttu-id="4f379-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f379-112">-DefaultProfile</span></span>
<span data-ttu-id="4f379-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f379-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f379-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f379-114">-Name</span></span>
<span data-ttu-id="4f379-115">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4f379-115">Resource name.</span></span>

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

### <span data-ttu-id="4f379-116">-Escopo</span><span class="sxs-lookup"><span data-stu-id="4f379-116">-Scope</span></span>
<span data-ttu-id="4f379-117">Escopo.</span><span class="sxs-lookup"><span data-stu-id="4f379-117">Scope.</span></span>

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

### <span data-ttu-id="4f379-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="4f379-118">-WorkspaceId</span></span>
<span data-ttu-id="4f379-119">ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4f379-119">Workspace ID.</span></span>

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

### <span data-ttu-id="4f379-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4f379-120">-Confirm</span></span>
<span data-ttu-id="4f379-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f379-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f379-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f379-122">-WhatIf</span></span>
<span data-ttu-id="4f379-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4f379-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f379-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f379-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f379-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f379-125">CommonParameters</span></span>
<span data-ttu-id="4f379-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f379-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f379-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f379-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f379-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="4f379-128">INPUTS</span></span>

### <span data-ttu-id="4f379-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4f379-129">System.String</span></span>

## <span data-ttu-id="4f379-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="4f379-130">OUTPUTS</span></span>

### <span data-ttu-id="4f379-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="4f379-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="4f379-132">Notas</span><span class="sxs-lookup"><span data-stu-id="4f379-132">NOTES</span></span>

## <span data-ttu-id="4f379-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f379-133">RELATED LINKS</span></span>
