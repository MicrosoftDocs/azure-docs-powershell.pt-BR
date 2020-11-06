---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: d785cd364cd67a9d79f8710ef664048b8f54b8ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430687"
---
# <span data-ttu-id="ce095-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="ce095-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="ce095-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce095-102">SYNOPSIS</span></span>
<span data-ttu-id="ce095-103">Permitir que a credencial do Azure, a conta e as informações de assinatura sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce095-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce095-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce095-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce095-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce095-105">DESCRIPTION</span></span>
<span data-ttu-id="ce095-106">Permitir que a credencial do Azure, a conta e as informações de assinatura sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce095-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="ce095-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce095-107">EXAMPLES</span></span>

### <span data-ttu-id="ce095-108">Habilitar a gravação simultânea de credenciais para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="ce095-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="ce095-109">Ative o salvamento automático de credenciais para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="ce095-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="ce095-110">Sempre que uma janela do PowerShell é aberta, seu contexto atual será lembrado sem fazer logon.</span><span class="sxs-lookup"><span data-stu-id="ce095-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="ce095-111">OS</span><span class="sxs-lookup"><span data-stu-id="ce095-111">PARAMETERS</span></span>

### <span data-ttu-id="ce095-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce095-112">-DefaultProfile</span></span>
<span data-ttu-id="ce095-113">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ce095-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce095-114">-Escopo</span><span class="sxs-lookup"><span data-stu-id="ce095-114">-Scope</span></span>
<span data-ttu-id="ce095-115">Determina o escopo das alterações de contexto, por exemplo, wheher alterações se aplicam somente ao processo cusrrent ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="ce095-115">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="ce095-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce095-116">-Confirm</span></span>
<span data-ttu-id="ce095-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce095-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce095-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce095-118">-WhatIf</span></span>
<span data-ttu-id="ce095-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce095-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce095-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce095-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce095-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce095-121">CommonParameters</span></span>
<span data-ttu-id="ce095-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce095-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce095-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce095-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce095-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce095-124">INPUTS</span></span>

### <span data-ttu-id="ce095-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ce095-125">None</span></span>

## <span data-ttu-id="ce095-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce095-126">OUTPUTS</span></span>

### <span data-ttu-id="ce095-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="ce095-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="ce095-128">Informações sobre as configurações atuais de salvamento automático, incluindo se o salvamento automático está habilitado para o usuário atual e onde os arquivos de contexto e credenciais são salvos.</span><span class="sxs-lookup"><span data-stu-id="ce095-128">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="ce095-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce095-129">NOTES</span></span>

## <span data-ttu-id="ce095-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce095-130">RELATED LINKS</span></span>
