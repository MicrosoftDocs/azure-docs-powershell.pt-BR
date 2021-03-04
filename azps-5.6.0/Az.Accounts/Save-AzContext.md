---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: f73ca19ffa2c68599a5244d41b39d90ebbd2835a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888343"
---
# <span data-ttu-id="a682e-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="a682e-101">Save-AzContext</span></span>

## <span data-ttu-id="a682e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a682e-102">SYNOPSIS</span></span>
<span data-ttu-id="a682e-103">Salva as informações de autenticação atuais para uso em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a682e-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="a682e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a682e-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a682e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a682e-105">DESCRIPTION</span></span>
<span data-ttu-id="a682e-106">O Save-AzContext cmdlet salva as informações de autenticação atuais para uso em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a682e-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="a682e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a682e-107">EXAMPLES</span></span>

### <span data-ttu-id="a682e-108">Exemplo 1: Salvar o contexto da sessão atual</span><span class="sxs-lookup"><span data-stu-id="a682e-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="a682e-109">Este exemplo salva o contexto do Azure da sessão atual no arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="a682e-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="a682e-110">Exemplo 2: Salvar um determinado contexto</span><span class="sxs-lookup"><span data-stu-id="a682e-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="a682e-111">Este exemplo salva o contexto do Azure que é passado para o cmdlet para o arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="a682e-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="a682e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a682e-112">PARAMETERS</span></span>

### <span data-ttu-id="a682e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a682e-113">-DefaultProfile</span></span>
<span data-ttu-id="a682e-114">As credenciais, locatários e assinaturas usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a682e-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a682e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a682e-115">-Force</span></span>
<span data-ttu-id="a682e-116">Substituir o arquivo determinado se ele existir</span><span class="sxs-lookup"><span data-stu-id="a682e-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="a682e-117">-Path</span><span class="sxs-lookup"><span data-stu-id="a682e-117">-Path</span></span>
<span data-ttu-id="a682e-118">Especifica o caminho do arquivo para o qual salvar informações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="a682e-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="a682e-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="a682e-119">-Profile</span></span>
<span data-ttu-id="a682e-120">Especifica o contexto do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a682e-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="a682e-121">Se você não especificar um contexto, esse cmdlet será lido do contexto padrão local.</span><span class="sxs-lookup"><span data-stu-id="a682e-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a682e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a682e-122">-Confirm</span></span>
<span data-ttu-id="a682e-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a682e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a682e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a682e-124">-WhatIf</span></span>
<span data-ttu-id="a682e-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a682e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a682e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a682e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a682e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a682e-127">CommonParameters</span></span>
<span data-ttu-id="a682e-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a682e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a682e-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a682e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a682e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a682e-130">INPUTS</span></span>

### <span data-ttu-id="a682e-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="a682e-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="a682e-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a682e-132">OUTPUTS</span></span>

### <span data-ttu-id="a682e-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a682e-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="a682e-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="a682e-134">NOTES</span></span>

## <span data-ttu-id="a682e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a682e-135">RELATED LINKS</span></span>
