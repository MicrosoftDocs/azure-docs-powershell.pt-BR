---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 679b1458b3e749b2ccfca3863f745edd562ffc2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599221"
---
# <span data-ttu-id="21a8d-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="21a8d-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="21a8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="21a8d-103">Atualiza as configurações do espaço de trabalho para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="21a8d-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="21a8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21a8d-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21a8d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21a8d-105">DESCRIPTION</span></span>
<span data-ttu-id="21a8d-106">Atualiza as configurações do espaço de trabalho para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="21a8d-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="21a8d-107">O espaço de trabalho configurado manterá os dados de segurança coletados pelo agente de segurança instalado em VMs dentro desta assinatura.</span><span class="sxs-lookup"><span data-stu-id="21a8d-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="21a8d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21a8d-108">EXAMPLES</span></span>

### <span data-ttu-id="21a8d-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21a8d-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="21a8d-110">Define o espaço de trabalho "MyWorkspace" para armazenar todos os dados de segurança coletados pelos agentes de segurança.</span><span class="sxs-lookup"><span data-stu-id="21a8d-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="21a8d-111">OS</span><span class="sxs-lookup"><span data-stu-id="21a8d-111">PARAMETERS</span></span>

### <span data-ttu-id="21a8d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a8d-112">-DefaultProfile</span></span>
<span data-ttu-id="21a8d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21a8d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a8d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="21a8d-114">-Name</span></span>
<span data-ttu-id="21a8d-115">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="21a8d-115">Resource name.</span></span>

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

### <span data-ttu-id="21a8d-116">-Escopo</span><span class="sxs-lookup"><span data-stu-id="21a8d-116">-Scope</span></span>
<span data-ttu-id="21a8d-117">Com.</span><span class="sxs-lookup"><span data-stu-id="21a8d-117">Scope.</span></span>

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

### <span data-ttu-id="21a8d-118">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="21a8d-118">-WorkspaceId</span></span>
<span data-ttu-id="21a8d-119">ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="21a8d-119">Workspace ID.</span></span>

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

### <span data-ttu-id="21a8d-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21a8d-120">-Confirm</span></span>
<span data-ttu-id="21a8d-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21a8d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21a8d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a8d-122">-WhatIf</span></span>
<span data-ttu-id="21a8d-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21a8d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21a8d-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21a8d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21a8d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a8d-125">CommonParameters</span></span>
<span data-ttu-id="21a8d-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a8d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a8d-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21a8d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a8d-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21a8d-128">INPUTS</span></span>

### <span data-ttu-id="21a8d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="21a8d-129">System.String</span></span>

## <span data-ttu-id="21a8d-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21a8d-130">OUTPUTS</span></span>

### <span data-ttu-id="21a8d-131">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="21a8d-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="21a8d-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21a8d-132">NOTES</span></span>

## <span data-ttu-id="21a8d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21a8d-133">RELATED LINKS</span></span>
