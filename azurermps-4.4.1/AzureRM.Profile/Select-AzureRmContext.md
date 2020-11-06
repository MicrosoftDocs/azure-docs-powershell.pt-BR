---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: 5450939ba5d0dc2fb1ae6c475d51b6fc9187082c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603344"
---
# <span data-ttu-id="93b56-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="93b56-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="93b56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93b56-102">SYNOPSIS</span></span>
<span data-ttu-id="93b56-103">Selecione uma assinatura e uma conta para direcionar nos cmdlets do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="93b56-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93b56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93b56-104">SYNTAX</span></span>

### <span data-ttu-id="93b56-105">Objeto de entrada (padrão)</span><span class="sxs-lookup"><span data-stu-id="93b56-105">Input Object (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93b56-106">Nome do contexto</span><span class="sxs-lookup"><span data-stu-id="93b56-106">Context Name</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="93b56-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93b56-107">DESCRIPTION</span></span>
<span data-ttu-id="93b56-108">Selecione uma assinatura para direcionar (ou conta ou locatário) nos cmdlets do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="93b56-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="93b56-109">Após esse cmdlet, cmdlets futuros direcionarão o contexto selecionado.</span><span class="sxs-lookup"><span data-stu-id="93b56-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="93b56-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93b56-110">EXAMPLES</span></span>

### <span data-ttu-id="93b56-111">Exemplo 1: direcionar um contexto nomeado</span><span class="sxs-lookup"><span data-stu-id="93b56-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="93b56-112">Direcione cmdlets futuros do PowerShell do Azure na conta, no locatário e na assinatura no contexto ' trabalho '.</span><span class="sxs-lookup"><span data-stu-id="93b56-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="93b56-113">OS</span><span class="sxs-lookup"><span data-stu-id="93b56-113">PARAMETERS</span></span>

### <span data-ttu-id="93b56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b56-114">-DefaultProfile</span></span>
<span data-ttu-id="93b56-115">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="93b56-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93b56-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93b56-116">-InputObject</span></span>
<span data-ttu-id="93b56-117">Um objeto Context, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="93b56-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93b56-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="93b56-118">-Name</span></span>
<span data-ttu-id="93b56-119">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="93b56-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b56-120">-Escopo</span><span class="sxs-lookup"><span data-stu-id="93b56-120">-Scope</span></span>
<span data-ttu-id="93b56-121">Determina o escopo das alterações de contexto, por exemplo, wheher alterações se aplicam somente ao processo cusrrent ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="93b56-121">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="93b56-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93b56-122">-Confirm</span></span>
<span data-ttu-id="93b56-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93b56-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93b56-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93b56-124">-WhatIf</span></span>
<span data-ttu-id="93b56-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93b56-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93b56-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93b56-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93b56-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b56-127">CommonParameters</span></span>
<span data-ttu-id="93b56-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93b56-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b56-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b56-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b56-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93b56-130">INPUTS</span></span>

### <span data-ttu-id="93b56-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="93b56-131">None</span></span>

## <span data-ttu-id="93b56-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93b56-132">OUTPUTS</span></span>

### <span data-ttu-id="93b56-133">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="93b56-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="93b56-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93b56-134">NOTES</span></span>

## <span data-ttu-id="93b56-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93b56-135">RELATED LINKS</span></span>

