---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 14bda211d79e871d71bdef320df552b592fb1b89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428411"
---
# <span data-ttu-id="1112b-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="1112b-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="1112b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1112b-102">SYNOPSIS</span></span>
<span data-ttu-id="1112b-103">Remova todas as credenciais do Azure, conta e informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="1112b-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1112b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1112b-104">SYNTAX</span></span>

```
Clear-AzureRmContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1112b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1112b-105">DESCRIPTION</span></span>
<span data-ttu-id="1112b-106">Remova todas as credenciais do Azure, conta e informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="1112b-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="1112b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1112b-107">EXAMPLES</span></span>

### <span data-ttu-id="1112b-108">Limpar contexto global</span><span class="sxs-lookup"><span data-stu-id="1112b-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="1112b-109">Remova todas as informações de conta, assinatura e credenciais para qualquer sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1112b-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="1112b-110">OS</span><span class="sxs-lookup"><span data-stu-id="1112b-110">PARAMETERS</span></span>

### <span data-ttu-id="1112b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1112b-111">-DefaultProfile</span></span>
<span data-ttu-id="1112b-112">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1112b-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1112b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1112b-113">-Force</span></span>
<span data-ttu-id="1112b-114">Excluir todos os usuários e grupos do escopo global sem solicitação</span><span class="sxs-lookup"><span data-stu-id="1112b-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="1112b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1112b-115">-PassThru</span></span>
<span data-ttu-id="1112b-116">Retornar um valor que indica êxito ou falha</span><span class="sxs-lookup"><span data-stu-id="1112b-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="1112b-117">-Escopo</span><span class="sxs-lookup"><span data-stu-id="1112b-117">-Scope</span></span>
<span data-ttu-id="1112b-118">Limpe o contexto somente para a sessão atual do PowerShell ou para todas as sessões.</span><span class="sxs-lookup"><span data-stu-id="1112b-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="1112b-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1112b-119">-Confirm</span></span>
<span data-ttu-id="1112b-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1112b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1112b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1112b-121">-WhatIf</span></span>
<span data-ttu-id="1112b-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1112b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1112b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1112b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1112b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1112b-124">CommonParameters</span></span>
<span data-ttu-id="1112b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1112b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1112b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1112b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1112b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1112b-127">INPUTS</span></span>

### <span data-ttu-id="1112b-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1112b-128">None</span></span>

## <span data-ttu-id="1112b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1112b-129">OUTPUTS</span></span>

### <span data-ttu-id="1112b-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1112b-130">System.Boolean</span></span>

## <span data-ttu-id="1112b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1112b-131">NOTES</span></span>

## <span data-ttu-id="1112b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1112b-132">RELATED LINKS</span></span>
