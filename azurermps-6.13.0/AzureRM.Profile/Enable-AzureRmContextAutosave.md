---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: ef36772679cb6d34ad469c6d78550634e6dec954
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610538"
---
# <span data-ttu-id="bcfac-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="bcfac-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="bcfac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcfac-102">SYNOPSIS</span></span>
<span data-ttu-id="bcfac-103">Permitir que a credencial do Azure, a conta e as informações de assinatura sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bcfac-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcfac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcfac-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcfac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcfac-105">DESCRIPTION</span></span>
<span data-ttu-id="bcfac-106">Permitir que a credencial do Azure, a conta e as informações de assinatura sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bcfac-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="bcfac-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcfac-107">EXAMPLES</span></span>

### <span data-ttu-id="bcfac-108">Habilitar a gravação simultânea de credenciais para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="bcfac-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="bcfac-109">Ative o salvamento automático de credenciais para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="bcfac-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="bcfac-110">Sempre que uma janela do PowerShell é aberta, seu contexto atual será lembrado sem fazer logon.</span><span class="sxs-lookup"><span data-stu-id="bcfac-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="bcfac-111">OS</span><span class="sxs-lookup"><span data-stu-id="bcfac-111">PARAMETERS</span></span>

### <span data-ttu-id="bcfac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcfac-112">-DefaultProfile</span></span>
<span data-ttu-id="bcfac-113">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bcfac-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcfac-114">-Escopo</span><span class="sxs-lookup"><span data-stu-id="bcfac-114">-Scope</span></span>
<span data-ttu-id="bcfac-115">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="bcfac-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="bcfac-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bcfac-116">-Confirm</span></span>
<span data-ttu-id="bcfac-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcfac-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcfac-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcfac-118">-WhatIf</span></span>
<span data-ttu-id="bcfac-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bcfac-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcfac-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bcfac-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcfac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcfac-121">CommonParameters</span></span>
<span data-ttu-id="bcfac-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcfac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcfac-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcfac-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcfac-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcfac-124">INPUTS</span></span>

### <span data-ttu-id="bcfac-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bcfac-125">None</span></span>

## <span data-ttu-id="bcfac-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcfac-126">OUTPUTS</span></span>

### <span data-ttu-id="bcfac-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="bcfac-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="bcfac-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcfac-128">NOTES</span></span>

## <span data-ttu-id="bcfac-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcfac-129">RELATED LINKS</span></span>
