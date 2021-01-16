---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432822"
---
# <span data-ttu-id="4c821-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="4c821-101">Save-AzContext</span></span>

## <span data-ttu-id="4c821-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c821-102">SYNOPSIS</span></span>
<span data-ttu-id="4c821-103">Salva as informações de autenticação atuais para usar em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c821-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="4c821-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c821-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c821-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c821-105">DESCRIPTION</span></span>
<span data-ttu-id="4c821-106">O cmdlet Save-AzContext salva as informações de autenticação atuais para uso em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c821-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="4c821-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c821-107">EXAMPLES</span></span>

### <span data-ttu-id="4c821-108">Exemplo 1: salvando o contexto da sessão atual</span><span class="sxs-lookup"><span data-stu-id="4c821-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="4c821-109">Este exemplo salva o contexto do Azure da sessão atual no arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="4c821-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="4c821-110">Exemplo 2: salvando um determinado contexto</span><span class="sxs-lookup"><span data-stu-id="4c821-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="4c821-111">Este exemplo salva o contexto do Azure que é passado para o cmdlet para o arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="4c821-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="4c821-112">OS</span><span class="sxs-lookup"><span data-stu-id="4c821-112">PARAMETERS</span></span>

### <span data-ttu-id="4c821-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c821-113">-DefaultProfile</span></span>
<span data-ttu-id="4c821-114">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c821-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c821-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4c821-115">-Force</span></span>
<span data-ttu-id="4c821-116">Substituir o arquivo fornecido se ele existir</span><span class="sxs-lookup"><span data-stu-id="4c821-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="4c821-117">-Caminho</span><span class="sxs-lookup"><span data-stu-id="4c821-117">-Path</span></span>
<span data-ttu-id="4c821-118">Especifica o caminho do arquivo no qual as informações de autenticação são salvas.</span><span class="sxs-lookup"><span data-stu-id="4c821-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="4c821-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4c821-119">-Profile</span></span>
<span data-ttu-id="4c821-120">Especifica o contexto do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4c821-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="4c821-121">Se você não especificar um contexto, esse cmdlet lerá do contexto padrão local.</span><span class="sxs-lookup"><span data-stu-id="4c821-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="4c821-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c821-122">-Confirm</span></span>
<span data-ttu-id="4c821-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c821-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c821-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c821-124">-WhatIf</span></span>
<span data-ttu-id="4c821-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c821-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c821-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c821-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c821-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c821-127">CommonParameters</span></span>
<span data-ttu-id="4c821-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c821-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c821-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c821-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c821-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c821-130">INPUTS</span></span>

### <span data-ttu-id="4c821-131">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="4c821-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="4c821-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c821-132">OUTPUTS</span></span>

### <span data-ttu-id="4c821-133">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="4c821-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="4c821-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c821-134">NOTES</span></span>

## <span data-ttu-id="4c821-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c821-135">RELATED LINKS</span></span>
