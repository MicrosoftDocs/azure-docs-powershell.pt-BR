---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425918"
---
# <span data-ttu-id="82371-101">Save-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="82371-101">Save-AzureRmProfile</span></span>

## <span data-ttu-id="82371-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82371-102">SYNOPSIS</span></span>
<span data-ttu-id="82371-103">Salva as informações de autenticação atuais para usar em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="82371-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="82371-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82371-104">SYNTAX</span></span>

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82371-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82371-105">DESCRIPTION</span></span>
<span data-ttu-id="82371-106">O cmdlet Save-AzureRmProfile salva as informações de autenticação atuais para uso em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="82371-106">The Save-AzureRmProfile cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="82371-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82371-107">EXAMPLES</span></span>

### <span data-ttu-id="82371-108">Exemplo 1: salvando o perfil da sessão atual</span><span class="sxs-lookup"><span data-stu-id="82371-108">Example 1: Saving the current session's profile</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

<span data-ttu-id="82371-109">Este exemplo salva o perfil do Azure da sessão atual no arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="82371-109">This example saves the current session's Azure profile to the JSON file provided.</span></span>

### <span data-ttu-id="82371-110">Exemplo 2: salvando um determinado perfil</span><span class="sxs-lookup"><span data-stu-id="82371-110">Example 2: Saving a given profile</span></span>
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="82371-111">Este exemplo salva o perfil do Azure que é passado para o cmdlet para o arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="82371-111">This example saves the Azure profile that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="82371-112">OS</span><span class="sxs-lookup"><span data-stu-id="82371-112">PARAMETERS</span></span>

### <span data-ttu-id="82371-113">-Force</span><span class="sxs-lookup"><span data-stu-id="82371-113">-Force</span></span>
<span data-ttu-id="82371-114">Substituir o arquivo fornecido se ele existir</span><span class="sxs-lookup"><span data-stu-id="82371-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82371-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="82371-115">-Path</span></span>
<span data-ttu-id="82371-116">Especifica o caminho do arquivo no qual as informações de autenticação são salvas.</span><span class="sxs-lookup"><span data-stu-id="82371-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82371-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="82371-117">-Profile</span></span>
<span data-ttu-id="82371-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="82371-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82371-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="82371-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82371-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="82371-120">-Confirm</span></span>
<span data-ttu-id="82371-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82371-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82371-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82371-122">-WhatIf</span></span>
<span data-ttu-id="82371-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="82371-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82371-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="82371-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82371-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82371-125">CommonParameters</span></span>
<span data-ttu-id="82371-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82371-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82371-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82371-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82371-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82371-128">INPUTS</span></span>

## <span data-ttu-id="82371-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82371-129">OUTPUTS</span></span>

### <span data-ttu-id="82371-130">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="82371-130">PSAzureProfile</span></span>

## <span data-ttu-id="82371-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82371-131">NOTES</span></span>

## <span data-ttu-id="82371-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82371-132">RELATED LINKS</span></span>

[<span data-ttu-id="82371-133">Select-AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="82371-133">Select-AzureRMProfile</span></span>]()

