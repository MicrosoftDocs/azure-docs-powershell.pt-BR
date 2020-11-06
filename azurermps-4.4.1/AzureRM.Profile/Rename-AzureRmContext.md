---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 9c9c0c3c52f610c0bb2c0198e9995cf2804b2b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610742"
---
# <span data-ttu-id="a004c-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a004c-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="a004c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a004c-102">SYNOPSIS</span></span>
<span data-ttu-id="a004c-103">Renomear um contexto do Azure.</span><span class="sxs-lookup"><span data-stu-id="a004c-103">Rename an Azure context.</span></span>  <span data-ttu-id="a004c-104">Por contextos padrão são nomeados por conta de usuário e assinatura.</span><span class="sxs-lookup"><span data-stu-id="a004c-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a004c-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a004c-105">SYNTAX</span></span>

### <span data-ttu-id="a004c-106">Objeto de entrada (padrão)</span><span class="sxs-lookup"><span data-stu-id="a004c-106">Input Object (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="a004c-107">Nome do contexto</span><span class="sxs-lookup"><span data-stu-id="a004c-107">Context Name</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="a004c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a004c-108">DESCRIPTION</span></span>
<span data-ttu-id="a004c-109">Renomear um contexto do Azure.</span><span class="sxs-lookup"><span data-stu-id="a004c-109">Rename an Azure context.</span></span>  <span data-ttu-id="a004c-110">Por contextos padrão são nomeados por conta de usuário e assinatura.</span><span class="sxs-lookup"><span data-stu-id="a004c-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="a004c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a004c-111">EXAMPLES</span></span>

### <span data-ttu-id="a004c-112">Renomear um contexto usando parâmetros nomeados</span><span class="sxs-lookup"><span data-stu-id="a004c-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="a004c-113">Renomeie o contexto de ' user1@contoso.org ' com a assinatura ' 12345-6789-2345-3567890 ' para ' trabalho '.</span><span class="sxs-lookup"><span data-stu-id="a004c-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="a004c-114">Após esse comando, você poderá direcionar o contexto usando o ' trabalho de seleção AzureRmContext '.</span><span class="sxs-lookup"><span data-stu-id="a004c-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="a004c-115">Observe que você pode Tab para percorrer os valores de ' SourceName ' usando a conclusão de tabulação.</span><span class="sxs-lookup"><span data-stu-id="a004c-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="a004c-116">Renomear um contexto usando parâmetros posicionais</span><span class="sxs-lookup"><span data-stu-id="a004c-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="a004c-117">Renomeie o contexto chamado "My Context" para "Work".</span><span class="sxs-lookup"><span data-stu-id="a004c-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="a004c-118">Após esse comando, você poderá direcionar o contexto usando Select-AzureRmContext trabalho</span><span class="sxs-lookup"><span data-stu-id="a004c-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="a004c-119">OS</span><span class="sxs-lookup"><span data-stu-id="a004c-119">PARAMETERS</span></span>

### <span data-ttu-id="a004c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a004c-120">-DefaultProfile</span></span>
<span data-ttu-id="a004c-121">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a004c-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a004c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a004c-122">-Force</span></span>
<span data-ttu-id="a004c-123">Renomeie o contexto mesmo se o contexto de destino já existir</span><span class="sxs-lookup"><span data-stu-id="a004c-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="a004c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a004c-124">-InputObject</span></span>
<span data-ttu-id="a004c-125">Um objeto Context, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a004c-125">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a004c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a004c-126">-PassThru</span></span>
<span data-ttu-id="a004c-127">Retorne o contexto renomeado.</span><span class="sxs-lookup"><span data-stu-id="a004c-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="a004c-128">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a004c-128">-Scope</span></span>
<span data-ttu-id="a004c-129">Determina o escopo das alterações de contexto, por exemplo, wheher alterações se aplicam somente ao processo cusrrent ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="a004c-129">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="a004c-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="a004c-130">-SourceName</span></span>
<span data-ttu-id="a004c-131">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="a004c-131">The name of the context</span></span>

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

### <span data-ttu-id="a004c-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="a004c-132">-TargetName</span></span>
<span data-ttu-id="a004c-133">O novo nome do contexto</span><span class="sxs-lookup"><span data-stu-id="a004c-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a004c-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a004c-134">-Confirm</span></span>
<span data-ttu-id="a004c-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a004c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a004c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a004c-136">-WhatIf</span></span>
<span data-ttu-id="a004c-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a004c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a004c-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a004c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a004c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a004c-139">CommonParameters</span></span>
<span data-ttu-id="a004c-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a004c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a004c-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a004c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a004c-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a004c-142">INPUTS</span></span>

### <span data-ttu-id="a004c-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a004c-143">None</span></span>

## <span data-ttu-id="a004c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a004c-144">OUTPUTS</span></span>

### <span data-ttu-id="a004c-145">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a004c-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="a004c-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a004c-146">NOTES</span></span>

## <span data-ttu-id="a004c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a004c-147">RELATED LINKS</span></span>

