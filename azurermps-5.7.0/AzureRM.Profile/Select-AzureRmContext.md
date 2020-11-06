---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/select-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: c002db2d04905c19c3229a45feb9e00b5dc15754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439843"
---
# <span data-ttu-id="4ba66-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="4ba66-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="4ba66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ba66-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba66-103">Selecione uma assinatura e uma conta para direcionar nos cmdlets do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4ba66-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ba66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ba66-104">SYNTAX</span></span>

### <span data-ttu-id="4ba66-105">SelectByInputObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ba66-105">SelectByInputObject (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ba66-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="4ba66-106">SelectByName</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="4ba66-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ba66-107">DESCRIPTION</span></span>
<span data-ttu-id="4ba66-108">Selecione uma assinatura para direcionar (ou conta ou locatário) nos cmdlets do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba66-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="4ba66-109">Após esse cmdlet, cmdlets futuros direcionarão o contexto selecionado.</span><span class="sxs-lookup"><span data-stu-id="4ba66-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="4ba66-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ba66-110">EXAMPLES</span></span>

### <span data-ttu-id="4ba66-111">Exemplo 1: direcionar um contexto nomeado</span><span class="sxs-lookup"><span data-stu-id="4ba66-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="4ba66-112">Direcione cmdlets futuros do PowerShell do Azure na conta, no locatário e na assinatura no contexto ' trabalho '.</span><span class="sxs-lookup"><span data-stu-id="4ba66-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="4ba66-113">OS</span><span class="sxs-lookup"><span data-stu-id="4ba66-113">PARAMETERS</span></span>

### <span data-ttu-id="4ba66-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba66-114">-DefaultProfile</span></span>
<span data-ttu-id="4ba66-115">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4ba66-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ba66-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ba66-116">-InputObject</span></span>
<span data-ttu-id="4ba66-117">Um objeto Context, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ba66-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: SelectByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba66-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ba66-118">-Name</span></span>
<span data-ttu-id="4ba66-119">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="4ba66-119">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: SelectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba66-120">-Escopo</span><span class="sxs-lookup"><span data-stu-id="4ba66-120">-Scope</span></span>
<span data-ttu-id="4ba66-121">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="4ba66-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba66-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ba66-122">-Confirm</span></span>
<span data-ttu-id="4ba66-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ba66-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba66-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba66-124">-WhatIf</span></span>
<span data-ttu-id="4ba66-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ba66-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ba66-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ba66-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba66-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba66-127">CommonParameters</span></span>
<span data-ttu-id="4ba66-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ba66-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba66-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba66-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba66-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ba66-130">INPUTS</span></span>

### <span data-ttu-id="4ba66-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4ba66-131">None</span></span>

## <span data-ttu-id="4ba66-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ba66-132">OUTPUTS</span></span>

### <span data-ttu-id="4ba66-133">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="4ba66-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="4ba66-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ba66-134">NOTES</span></span>

## <span data-ttu-id="4ba66-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ba66-135">RELATED LINKS</span></span>

