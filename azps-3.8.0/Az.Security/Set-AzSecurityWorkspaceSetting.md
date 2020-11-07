---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 2e74751b3f64c3192e7983188ae66cde021f0e3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943764"
---
# <span data-ttu-id="06e48-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="06e48-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="06e48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06e48-102">SYNOPSIS</span></span>
<span data-ttu-id="06e48-103">Atualiza as configurações do espaço de trabalho para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="06e48-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="06e48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06e48-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06e48-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06e48-105">DESCRIPTION</span></span>
<span data-ttu-id="06e48-106">Atualiza as configurações do espaço de trabalho para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="06e48-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="06e48-107">O espaço de trabalho configurado manterá os dados de segurança coletados pelo agente do agente de análise de logs do Azure que está instalado em VMs dentro desta assinatura.</span><span class="sxs-lookup"><span data-stu-id="06e48-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="06e48-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06e48-108">EXAMPLES</span></span>

### <span data-ttu-id="06e48-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06e48-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="06e48-110">Define o espaço de trabalho "MyWorkspace" para armazenar todos os dados de segurança coletados pelo agente de análise de logs do Azure.</span><span class="sxs-lookup"><span data-stu-id="06e48-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="06e48-111">OS</span><span class="sxs-lookup"><span data-stu-id="06e48-111">PARAMETERS</span></span>

### <span data-ttu-id="06e48-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e48-112">-DefaultProfile</span></span>
<span data-ttu-id="06e48-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06e48-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06e48-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="06e48-114">-Name</span></span>
<span data-ttu-id="06e48-115">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="06e48-115">Resource name.</span></span>

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

### <span data-ttu-id="06e48-116">-Escopo</span><span class="sxs-lookup"><span data-stu-id="06e48-116">-Scope</span></span>
<span data-ttu-id="06e48-117">Com.</span><span class="sxs-lookup"><span data-stu-id="06e48-117">Scope.</span></span>

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

### <span data-ttu-id="06e48-118">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="06e48-118">-WorkspaceId</span></span>
<span data-ttu-id="06e48-119">ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="06e48-119">Workspace ID.</span></span>

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

### <span data-ttu-id="06e48-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="06e48-120">-Confirm</span></span>
<span data-ttu-id="06e48-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06e48-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e48-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e48-122">-WhatIf</span></span>
<span data-ttu-id="06e48-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06e48-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06e48-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06e48-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e48-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e48-125">CommonParameters</span></span>
<span data-ttu-id="06e48-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e48-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e48-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e48-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e48-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06e48-128">INPUTS</span></span>

### <span data-ttu-id="06e48-129">System. String</span><span class="sxs-lookup"><span data-stu-id="06e48-129">System.String</span></span>

## <span data-ttu-id="06e48-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06e48-130">OUTPUTS</span></span>

### <span data-ttu-id="06e48-131">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="06e48-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="06e48-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06e48-132">NOTES</span></span>

## <span data-ttu-id="06e48-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06e48-133">RELATED LINKS</span></span>
