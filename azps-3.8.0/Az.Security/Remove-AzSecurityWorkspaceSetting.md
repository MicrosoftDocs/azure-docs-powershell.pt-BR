---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 79780c101296d78115a1c88ef4d4aebcd3721c22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941583"
---
# <span data-ttu-id="b339a-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b339a-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b339a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b339a-102">SYNOPSIS</span></span>
<span data-ttu-id="b339a-103">Exclui a configuração de espaço de trabalho de segurança para esta assinatura.</span><span class="sxs-lookup"><span data-stu-id="b339a-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="b339a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b339a-104">SYNTAX</span></span>

### <span data-ttu-id="b339a-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="b339a-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b339a-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="b339a-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b339a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b339a-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b339a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b339a-108">DESCRIPTION</span></span>
<span data-ttu-id="b339a-109">Exclui a configuração de espaço de trabalho de segurança para esta assinatura.</span><span class="sxs-lookup"><span data-stu-id="b339a-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="b339a-110">Esta ação fará com que os agentes de segurança recém-instalados relatem ao espaço de trabalho padrão desta assinatura.</span><span class="sxs-lookup"><span data-stu-id="b339a-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="b339a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b339a-111">EXAMPLES</span></span>

### <span data-ttu-id="b339a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b339a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="b339a-113">Exclui a configuração de espaço de trabalho de segurança para esta assinatura.</span><span class="sxs-lookup"><span data-stu-id="b339a-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="b339a-114">OS</span><span class="sxs-lookup"><span data-stu-id="b339a-114">PARAMETERS</span></span>

### <span data-ttu-id="b339a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b339a-115">-DefaultProfile</span></span>
<span data-ttu-id="b339a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b339a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b339a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b339a-117">-InputObject</span></span>
<span data-ttu-id="b339a-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="b339a-118">Input Object.</span></span>

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

### <span data-ttu-id="b339a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b339a-119">-Name</span></span>
<span data-ttu-id="b339a-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b339a-120">Resource name.</span></span>

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

### <span data-ttu-id="b339a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b339a-121">-PassThru</span></span>
<span data-ttu-id="b339a-122">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b339a-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b339a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b339a-123">-ResourceId</span></span>
<span data-ttu-id="b339a-124">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b339a-124">Resource ID.</span></span>

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

### <span data-ttu-id="b339a-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b339a-125">-Confirm</span></span>
<span data-ttu-id="b339a-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b339a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b339a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b339a-127">-WhatIf</span></span>
<span data-ttu-id="b339a-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b339a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b339a-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b339a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b339a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b339a-130">CommonParameters</span></span>
<span data-ttu-id="b339a-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b339a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b339a-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b339a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b339a-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b339a-133">INPUTS</span></span>

### <span data-ttu-id="b339a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b339a-134">System.String</span></span>

### <span data-ttu-id="b339a-135">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b339a-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b339a-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b339a-136">OUTPUTS</span></span>

### <span data-ttu-id="b339a-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b339a-137">System.Boolean</span></span>

## <span data-ttu-id="b339a-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b339a-138">NOTES</span></span>

## <span data-ttu-id="b339a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b339a-139">RELATED LINKS</span></span>
