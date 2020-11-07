---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945483"
---
# <span data-ttu-id="ad0cb-101">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ad0cb-101">Remove-AzureWebsite</span></span>

## <span data-ttu-id="ad0cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0cb-103">Remove o site especificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-103">Removes the specified website from Azure.</span></span>

## <span data-ttu-id="ad0cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad0cb-104">SYNTAX</span></span>

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad0cb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad0cb-105">DESCRIPTION</span></span>
<span data-ttu-id="ad0cb-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ad0cb-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ad0cb-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ad0cb-108">O cmdlet **Remove-AzureWebsite** remove o site especificado do Azure, seja com ou sem solicitação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-108">The **Remove-AzureWebsite** cmdlet removes the specified website from Azure, either with or without a prompt for confirmation.</span></span>

## <span data-ttu-id="ad0cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad0cb-109">EXAMPLES</span></span>

### <span data-ttu-id="ad0cb-110">Exemplo 1: remover o site atual</span><span class="sxs-lookup"><span data-stu-id="ad0cb-110">Example 1: Remove the current website</span></span>
```
PS C:\> Remove-AzureWebsite
```

<span data-ttu-id="ad0cb-111">Este exemplo remove o site do Azure associado ao diretório atual.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-111">This example removes the website in Azure associated with the current directory.</span></span>

### <span data-ttu-id="ad0cb-112">Exemplo 2: remover um site sem confirmação</span><span class="sxs-lookup"><span data-stu-id="ad0cb-112">Example 2: Remove a website without confirmation</span></span>
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

<span data-ttu-id="ad0cb-113">Este exemplo exclui o website chamado meusite sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-113">This example deletes the website named mySite without prompting for confirmation.</span></span>

## <span data-ttu-id="ad0cb-114">OS</span><span class="sxs-lookup"><span data-stu-id="ad0cb-114">PARAMETERS</span></span>

### <span data-ttu-id="ad0cb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ad0cb-115">-Force</span></span>
<span data-ttu-id="ad0cb-116">Se especificado, exclui o site especificado sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-116">If specified, deletes the specified website without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad0cb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad0cb-117">-Name</span></span>
<span data-ttu-id="ad0cb-118">Especifica o nome do site a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-118">Specifies the name of the website to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad0cb-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ad0cb-119">-Profile</span></span>
<span data-ttu-id="ad0cb-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad0cb-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad0cb-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="ad0cb-122">-Slot</span></span>
<span data-ttu-id="ad0cb-123">Especifica o nome do slot do site.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-123">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad0cb-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ad0cb-124">-Confirm</span></span>
<span data-ttu-id="ad0cb-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad0cb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad0cb-126">-WhatIf</span></span>
<span data-ttu-id="ad0cb-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad0cb-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad0cb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0cb-129">CommonParameters</span></span>
<span data-ttu-id="ad0cb-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad0cb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0cb-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad0cb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0cb-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad0cb-132">INPUTS</span></span>

## <span data-ttu-id="ad0cb-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad0cb-133">OUTPUTS</span></span>

## <span data-ttu-id="ad0cb-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad0cb-134">NOTES</span></span>

## <span data-ttu-id="ad0cb-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad0cb-135">RELATED LINKS</span></span>

[<span data-ttu-id="ad0cb-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ad0cb-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


