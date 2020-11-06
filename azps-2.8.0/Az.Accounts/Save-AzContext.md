---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 337fbe8fbfd11fdedad3fa13279dac60bac08455
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598234"
---
# <span data-ttu-id="c9e90-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="c9e90-101">Save-AzContext</span></span>

## <span data-ttu-id="c9e90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9e90-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e90-103">Salva as informações de autenticação atuais para usar em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9e90-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="c9e90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9e90-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9e90-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9e90-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e90-106">O cmdlet Save-AzContext salva as informações de autenticação atuais para uso em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9e90-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="c9e90-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9e90-107">EXAMPLES</span></span>

### <span data-ttu-id="c9e90-108">Exemplo 1: salvando o contexto da sessão atual</span><span class="sxs-lookup"><span data-stu-id="c9e90-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="c9e90-109">Este exemplo salva o contexto do Azure da sessão atual no arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="c9e90-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="c9e90-110">Exemplo 2: salvando um determinado contexto</span><span class="sxs-lookup"><span data-stu-id="c9e90-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="c9e90-111">Este exemplo salva o contexto do Azure que é passado para o cmdlet para o arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="c9e90-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="c9e90-112">OS</span><span class="sxs-lookup"><span data-stu-id="c9e90-112">PARAMETERS</span></span>

### <span data-ttu-id="c9e90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e90-113">-DefaultProfile</span></span>
<span data-ttu-id="c9e90-114">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9e90-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9e90-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c9e90-115">-Force</span></span>
<span data-ttu-id="c9e90-116">Substituir o arquivo fornecido se ele existir</span><span class="sxs-lookup"><span data-stu-id="c9e90-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="c9e90-117">-Caminho</span><span class="sxs-lookup"><span data-stu-id="c9e90-117">-Path</span></span>
<span data-ttu-id="c9e90-118">Especifica o caminho do arquivo no qual as informações de autenticação são salvas.</span><span class="sxs-lookup"><span data-stu-id="c9e90-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="c9e90-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c9e90-119">-Profile</span></span>
<span data-ttu-id="c9e90-120">Especifica o contexto do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c9e90-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="c9e90-121">Se você não especificar um contexto, esse cmdlet lerá do contexto padrão local.</span><span class="sxs-lookup"><span data-stu-id="c9e90-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="c9e90-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c9e90-122">-Confirm</span></span>
<span data-ttu-id="c9e90-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9e90-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9e90-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9e90-124">-WhatIf</span></span>
<span data-ttu-id="c9e90-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9e90-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9e90-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9e90-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9e90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e90-127">CommonParameters</span></span>
<span data-ttu-id="c9e90-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9e90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e90-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9e90-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e90-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9e90-130">INPUTS</span></span>

### <span data-ttu-id="c9e90-131">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="c9e90-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="c9e90-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9e90-132">OUTPUTS</span></span>

### <span data-ttu-id="c9e90-133">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="c9e90-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="c9e90-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9e90-134">NOTES</span></span>

## <span data-ttu-id="c9e90-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9e90-135">RELATED LINKS</span></span>
