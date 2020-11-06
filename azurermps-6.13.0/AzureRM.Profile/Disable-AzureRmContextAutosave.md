---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: c421489490dcd579384b211619180209e9d71f5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440732"
---
# <span data-ttu-id="6a1ee-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="6a1ee-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="6a1ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a1ee-102">SYNOPSIS</span></span>
<span data-ttu-id="6a1ee-103">Desativar o salvamento de credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a1ee-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="6a1ee-104">Suas informações de login serão esquecidas na próxima vez que você abrir uma janela do PowerShell</span><span class="sxs-lookup"><span data-stu-id="6a1ee-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a1ee-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a1ee-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a1ee-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a1ee-106">DESCRIPTION</span></span>
<span data-ttu-id="6a1ee-107">Desativar o salvamento de credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a1ee-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="6a1ee-108">Suas informações de login serão esquecidas na próxima vez que você abrir uma janela do PowerShell</span><span class="sxs-lookup"><span data-stu-id="6a1ee-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="6a1ee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a1ee-109">EXAMPLES</span></span>

### <span data-ttu-id="6a1ee-110">Desabilitar o salvamento AutoTexto</span><span class="sxs-lookup"><span data-stu-id="6a1ee-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="6a1ee-111">Desabilitar o salvamento automático do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="6a1ee-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="6a1ee-112">OS</span><span class="sxs-lookup"><span data-stu-id="6a1ee-112">PARAMETERS</span></span>

### <span data-ttu-id="6a1ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a1ee-113">-DefaultProfile</span></span>
<span data-ttu-id="6a1ee-114">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6a1ee-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a1ee-115">-Escopo</span><span class="sxs-lookup"><span data-stu-id="6a1ee-115">-Scope</span></span>
<span data-ttu-id="6a1ee-116">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="6a1ee-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a1ee-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6a1ee-117">-Confirm</span></span>
<span data-ttu-id="6a1ee-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a1ee-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a1ee-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a1ee-119">-WhatIf</span></span>
<span data-ttu-id="6a1ee-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6a1ee-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a1ee-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a1ee-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a1ee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a1ee-122">CommonParameters</span></span>
<span data-ttu-id="6a1ee-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a1ee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a1ee-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a1ee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a1ee-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a1ee-125">INPUTS</span></span>

### <span data-ttu-id="6a1ee-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6a1ee-126">None</span></span>

## <span data-ttu-id="6a1ee-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a1ee-127">OUTPUTS</span></span>

### <span data-ttu-id="6a1ee-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="6a1ee-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="6a1ee-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a1ee-129">NOTES</span></span>

## <span data-ttu-id="6a1ee-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a1ee-130">RELATED LINKS</span></span>
