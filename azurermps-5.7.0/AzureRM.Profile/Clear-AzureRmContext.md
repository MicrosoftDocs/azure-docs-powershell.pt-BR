---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 960e1b35a90b0bc1c490cbf194c20ac7a051e4d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426662"
---
# <span data-ttu-id="df2bc-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="df2bc-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="df2bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="df2bc-103">Remova todas as credenciais do Azure, conta e informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="df2bc-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df2bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df2bc-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df2bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df2bc-105">DESCRIPTION</span></span>
<span data-ttu-id="df2bc-106">Remova todas as credenciais do Azure, conta e informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="df2bc-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="df2bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df2bc-107">EXAMPLES</span></span>

### <span data-ttu-id="df2bc-108">Limpar contexto global</span><span class="sxs-lookup"><span data-stu-id="df2bc-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="df2bc-109">Remova todas as informações de conta, assinatura e credenciais para qualquer sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="df2bc-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="df2bc-110">OS</span><span class="sxs-lookup"><span data-stu-id="df2bc-110">PARAMETERS</span></span>

### <span data-ttu-id="df2bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df2bc-111">-DefaultProfile</span></span>
<span data-ttu-id="df2bc-112">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="df2bc-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df2bc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="df2bc-113">-Force</span></span>
<span data-ttu-id="df2bc-114">Excluir todos os usuários e grupos do escopo global sem solicitação</span><span class="sxs-lookup"><span data-stu-id="df2bc-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="df2bc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df2bc-115">-PassThru</span></span>
<span data-ttu-id="df2bc-116">Retornar um valor que indica êxito ou falha</span><span class="sxs-lookup"><span data-stu-id="df2bc-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="df2bc-117">-Escopo</span><span class="sxs-lookup"><span data-stu-id="df2bc-117">-Scope</span></span>
<span data-ttu-id="df2bc-118">Limpe o contexto somente para a sessão atual do PowerShell ou para todas as sessões.</span><span class="sxs-lookup"><span data-stu-id="df2bc-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df2bc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df2bc-119">-Confirm</span></span>
<span data-ttu-id="df2bc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df2bc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df2bc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df2bc-121">-WhatIf</span></span>
<span data-ttu-id="df2bc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df2bc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df2bc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df2bc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df2bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df2bc-124">CommonParameters</span></span>
<span data-ttu-id="df2bc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df2bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df2bc-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df2bc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df2bc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df2bc-127">INPUTS</span></span>

### <span data-ttu-id="df2bc-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="df2bc-128">None</span></span>

## <span data-ttu-id="df2bc-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df2bc-129">OUTPUTS</span></span>

### <span data-ttu-id="df2bc-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df2bc-130">System.Boolean</span></span>
<span data-ttu-id="df2bc-131">True se o contexto for limpo com êxito; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="df2bc-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="df2bc-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df2bc-132">NOTES</span></span>

## <span data-ttu-id="df2bc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df2bc-133">RELATED LINKS</span></span>

