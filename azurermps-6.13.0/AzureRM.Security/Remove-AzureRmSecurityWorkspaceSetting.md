---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 1c6f6a38c1811bdda32b60d4af1707c78eb7afd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602581"
---
# <span data-ttu-id="74d76-101">Remove-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="74d76-101">Remove-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="74d76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74d76-102">SYNOPSIS</span></span>
<span data-ttu-id="74d76-103">Exclui a configuração de espaço de trabalho de segurança para esta assinatura.</span><span class="sxs-lookup"><span data-stu-id="74d76-103">Deletes the security workspace setting for this subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74d76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74d76-104">SYNTAX</span></span>

### <span data-ttu-id="74d76-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="74d76-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d76-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="74d76-106">ResourceId</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d76-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="74d76-107">InputObject</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -InputObject <PSRemoveWorkspaceSettingInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74d76-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74d76-108">DESCRIPTION</span></span>
<span data-ttu-id="74d76-109">Exclui a configuração de espaço de trabalho de segurança para esta assinatura.</span><span class="sxs-lookup"><span data-stu-id="74d76-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="74d76-110">Esta ação fará com que os agentes de segurança recém-instalados relatem ao espaço de trabalho padrão deste susbscription.</span><span class="sxs-lookup"><span data-stu-id="74d76-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="74d76-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74d76-111">EXAMPLES</span></span>

### <span data-ttu-id="74d76-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="74d76-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="74d76-113">Exclui a configuração de espaço de trabalho de segurança para esta assinatura.</span><span class="sxs-lookup"><span data-stu-id="74d76-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="74d76-114">OS</span><span class="sxs-lookup"><span data-stu-id="74d76-114">PARAMETERS</span></span>

### <span data-ttu-id="74d76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d76-115">-DefaultProfile</span></span>
<span data-ttu-id="74d76-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74d76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74d76-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74d76-117">-InputObject</span></span>
<span data-ttu-id="74d76-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="74d76-118">Input Object.</span></span>

```yaml
Type: PSRemoveWorkspaceSettingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74d76-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="74d76-119">-Name</span></span>
<span data-ttu-id="74d76-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="74d76-120">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d76-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74d76-121">-PassThru</span></span>
<span data-ttu-id="74d76-122">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="74d76-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="74d76-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74d76-123">-ResourceId</span></span>
<span data-ttu-id="74d76-124">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="74d76-124">Resource ID.</span></span>

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

### <span data-ttu-id="74d76-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="74d76-125">-Confirm</span></span>
<span data-ttu-id="74d76-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74d76-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d76-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d76-127">-WhatIf</span></span>
<span data-ttu-id="74d76-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74d76-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74d76-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74d76-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d76-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d76-130">CommonParameters</span></span>
<span data-ttu-id="74d76-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d76-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d76-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74d76-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d76-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74d76-133">INPUTS</span></span>

### <span data-ttu-id="74d76-134">System. String</span><span class="sxs-lookup"><span data-stu-id="74d76-134">System.String</span></span>
<span data-ttu-id="74d76-135">Microsoft. Azure. Commands. Security. cmdlets. WorkspaceSettings. PSRemoveWorkspaceSettingInputObject</span><span class="sxs-lookup"><span data-stu-id="74d76-135">Microsoft.Azure.Commands.Security.Cmdlets.WorkspaceSettings.PSRemoveWorkspaceSettingInputObject</span></span>

## <span data-ttu-id="74d76-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74d76-136">OUTPUTS</span></span>

### <span data-ttu-id="74d76-137">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="74d76-137">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="74d76-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74d76-138">NOTES</span></span>

## <span data-ttu-id="74d76-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74d76-139">RELATED LINKS</span></span>
