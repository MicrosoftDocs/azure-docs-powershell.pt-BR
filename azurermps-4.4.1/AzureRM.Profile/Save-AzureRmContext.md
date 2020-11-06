---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 5c6200f6d68760cbd93460b38cb72a379845e622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603346"
---
# <span data-ttu-id="fa548-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="fa548-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="fa548-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa548-102">SYNOPSIS</span></span>
<span data-ttu-id="fa548-103">Salva as informações de autenticação atuais para usar em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fa548-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa548-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa548-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa548-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa548-105">DESCRIPTION</span></span>
<span data-ttu-id="fa548-106">O cmdlet Save-AzureRmContext salva as informações de autenticação atuais para uso em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fa548-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="fa548-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa548-107">EXAMPLES</span></span>

### <span data-ttu-id="fa548-108">Exemplo 1: salvando o contexto da sessão atual</span><span class="sxs-lookup"><span data-stu-id="fa548-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="fa548-109">Este exemplo salva o contexto do Azure da sessão atual no arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="fa548-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="fa548-110">Exemplo 2: salvando um determinado contexto</span><span class="sxs-lookup"><span data-stu-id="fa548-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="fa548-111">Este exemplo salva o contexto do Azure que é passado para o cmdlet para o arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="fa548-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="fa548-112">OS</span><span class="sxs-lookup"><span data-stu-id="fa548-112">PARAMETERS</span></span>

### <span data-ttu-id="fa548-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa548-113">-DefaultProfile</span></span>
<span data-ttu-id="fa548-114">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa548-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa548-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fa548-115">-Force</span></span>
<span data-ttu-id="fa548-116">Substituir o arquivo fornecido se ele existir</span><span class="sxs-lookup"><span data-stu-id="fa548-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="fa548-117">-Caminho</span><span class="sxs-lookup"><span data-stu-id="fa548-117">-Path</span></span>
<span data-ttu-id="fa548-118">Especifica o caminho do arquivo no qual as informações de autenticação são salvas.</span><span class="sxs-lookup"><span data-stu-id="fa548-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="fa548-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="fa548-119">-Profile</span></span>
<span data-ttu-id="fa548-120">Especifica o contexto do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="fa548-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="fa548-121">Se você não especificar um contexto, esse cmdlet lerá do contexto padrão local.</span><span class="sxs-lookup"><span data-stu-id="fa548-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="fa548-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fa548-122">-Confirm</span></span>
<span data-ttu-id="fa548-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa548-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa548-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa548-124">-WhatIf</span></span>
<span data-ttu-id="fa548-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa548-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa548-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa548-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa548-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa548-127">CommonParameters</span></span>
<span data-ttu-id="fa548-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa548-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa548-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa548-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa548-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa548-130">INPUTS</span></span>

### <span data-ttu-id="fa548-131">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="fa548-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="fa548-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa548-132">OUTPUTS</span></span>

### <span data-ttu-id="fa548-133">Microsoft. Azure. Commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="fa548-133">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="fa548-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa548-134">NOTES</span></span>

## <span data-ttu-id="fa548-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa548-135">RELATED LINKS</span></span>

