---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: 8bc129ddc1b4291ea7b3c9100a964bf5bb1dcee6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440987"
---
# <span data-ttu-id="10cfd-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="10cfd-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="10cfd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="10cfd-103">Remover um contexto do conjunto de contextos disponíveis</span><span class="sxs-lookup"><span data-stu-id="10cfd-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10cfd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10cfd-104">SYNTAX</span></span>

### <span data-ttu-id="10cfd-105">Objeto de entrada (padrão)</span><span class="sxs-lookup"><span data-stu-id="10cfd-105">Input Object (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10cfd-106">Contexto nomeado</span><span class="sxs-lookup"><span data-stu-id="10cfd-106">Named Context</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="10cfd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10cfd-107">DESCRIPTION</span></span>
<span data-ttu-id="10cfd-108">Remover um contexto do Azure do conjunto de contextos</span><span class="sxs-lookup"><span data-stu-id="10cfd-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="10cfd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10cfd-109">EXAMPLES</span></span>

### <span data-ttu-id="10cfd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10cfd-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="10cfd-111">Remover o contexto chamado padrão</span><span class="sxs-lookup"><span data-stu-id="10cfd-111">Remove the context named default</span></span>

## <span data-ttu-id="10cfd-112">OS</span><span class="sxs-lookup"><span data-stu-id="10cfd-112">PARAMETERS</span></span>

### <span data-ttu-id="10cfd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10cfd-113">-DefaultProfile</span></span>
<span data-ttu-id="10cfd-114">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10cfd-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10cfd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="10cfd-115">-Force</span></span>
<span data-ttu-id="10cfd-116">Remover contexto mesmo que seja o</span><span class="sxs-lookup"><span data-stu-id="10cfd-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="10cfd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10cfd-117">-InputObject</span></span>
<span data-ttu-id="10cfd-118">Um objeto Context, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="10cfd-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="10cfd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="10cfd-119">-Name</span></span>
<span data-ttu-id="10cfd-120">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="10cfd-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Named Context
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cfd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10cfd-121">-PassThru</span></span>
<span data-ttu-id="10cfd-122">Retornar o contexto removido</span><span class="sxs-lookup"><span data-stu-id="10cfd-122">Return the removed context</span></span>

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

### <span data-ttu-id="10cfd-123">-Escopo</span><span class="sxs-lookup"><span data-stu-id="10cfd-123">-Scope</span></span>
<span data-ttu-id="10cfd-124">Determina o escopo das alterações de contexto, por exemplo, wheher alterações se aplicam somente ao processo cusrrent ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="10cfd-124">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="10cfd-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="10cfd-125">-Confirm</span></span>
<span data-ttu-id="10cfd-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10cfd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10cfd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10cfd-127">-WhatIf</span></span>
<span data-ttu-id="10cfd-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10cfd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10cfd-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10cfd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10cfd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cfd-130">CommonParameters</span></span>
<span data-ttu-id="10cfd-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10cfd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cfd-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10cfd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cfd-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10cfd-133">INPUTS</span></span>

### <span data-ttu-id="10cfd-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="10cfd-134">None</span></span>

## <span data-ttu-id="10cfd-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10cfd-135">OUTPUTS</span></span>

### <span data-ttu-id="10cfd-136">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="10cfd-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="10cfd-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10cfd-137">NOTES</span></span>

## <span data-ttu-id="10cfd-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10cfd-138">RELATED LINKS</span></span>

