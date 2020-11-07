---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 1ca2244d4ed1a47535a228ed772d9d9a6ecb6acb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941221"
---
# <span data-ttu-id="03aee-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="03aee-101">Select-AzProfile</span></span>

## <span data-ttu-id="03aee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03aee-102">SYNOPSIS</span></span>
<span data-ttu-id="03aee-103">Para módulos que dão suporte a vários perfis de serviço-carregue os cmdlets correspondentes a um determinado perfil de serviço.</span><span class="sxs-lookup"><span data-stu-id="03aee-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="03aee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03aee-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03aee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03aee-105">DESCRIPTION</span></span>
<span data-ttu-id="03aee-106">Para módulos que dão suporte a vários perfis de serviço-carregue os cmdlets correspondentes a um determinado perfil de serviço.</span><span class="sxs-lookup"><span data-stu-id="03aee-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="03aee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03aee-107">EXAMPLES</span></span>

### <span data-ttu-id="03aee-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03aee-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="03aee-109">Carregar cmdlets para o perfil do AzureStack a partir de março de 2019</span><span class="sxs-lookup"><span data-stu-id="03aee-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="03aee-110">OS</span><span class="sxs-lookup"><span data-stu-id="03aee-110">PARAMETERS</span></span>

### <span data-ttu-id="03aee-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="03aee-111">-Name</span></span>
<span data-ttu-id="03aee-112">O nome do perfil a ser selecionado</span><span class="sxs-lookup"><span data-stu-id="03aee-112">The name of the profile to select</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProfileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03aee-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03aee-113">-PassThru</span></span>
<span data-ttu-id="03aee-114">Quando presente, força o cmdlet a retornar um valor na execução bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="03aee-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="03aee-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03aee-115">-Confirm</span></span>
<span data-ttu-id="03aee-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03aee-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03aee-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03aee-117">-WhatIf</span></span>
<span data-ttu-id="03aee-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03aee-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03aee-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03aee-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03aee-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03aee-120">CommonParameters</span></span>
<span data-ttu-id="03aee-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03aee-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03aee-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03aee-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03aee-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03aee-123">INPUTS</span></span>

### <span data-ttu-id="03aee-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="03aee-124">None</span></span>

## <span data-ttu-id="03aee-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03aee-125">OUTPUTS</span></span>

### <span data-ttu-id="03aee-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="03aee-126">System.Object</span></span>
## <span data-ttu-id="03aee-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03aee-127">NOTES</span></span>

## <span data-ttu-id="03aee-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03aee-128">RELATED LINKS</span></span>
