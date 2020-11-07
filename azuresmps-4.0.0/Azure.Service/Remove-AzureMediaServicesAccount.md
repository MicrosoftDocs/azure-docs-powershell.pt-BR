---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5B255D11-0A9B-4679-A2AC-4357B293EE96
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4eee130312ae52e95b020151750d46144bc3685
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946471"
---
# <span data-ttu-id="a3cd1-101">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a3cd1-101">Remove-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="a3cd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="a3cd1-103">Remove a conta especificada do Azure Media Services.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-103">Removes the specified Azure Media Services account.</span></span>

<span data-ttu-id="a3cd1-104">**Observação:**  Esta versão foi preterida, confira a [versão mais recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="a3cd1-104">**Note:**  This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="a3cd1-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3cd1-105">SYNTAX</span></span>

```
Remove-AzureMediaServicesAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3cd1-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3cd1-106">DESCRIPTION</span></span>
<span data-ttu-id="a3cd1-107">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a3cd1-108">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a3cd1-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a3cd1-109">O cmdlet **Remove-AzureMediaServicesAccount** remove uma conta de serviços de mídia.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-109">The **Remove-AzureMediaServicesAccount** cmdlet removes a Media Services account.</span></span>

## <span data-ttu-id="a3cd1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3cd1-110">EXAMPLES</span></span>

### <span data-ttu-id="a3cd1-111">Exemplo 1: excluir uma conta de serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="a3cd1-111">Example 1: Delete a Media Services account</span></span>
```
PS C:\> Remove-AzureMediaServicesAccount -Name "mediaservicesaccount" -Force
```

## <span data-ttu-id="a3cd1-112">OS</span><span class="sxs-lookup"><span data-stu-id="a3cd1-112">PARAMETERS</span></span>

### <span data-ttu-id="a3cd1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a3cd1-113">-Force</span></span>
<span data-ttu-id="a3cd1-114">Se a opção *forçada* for especificada, a exclusão não será confirmada.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-114">If the *Force* switch is specified, the deletion is not confirmed.</span></span>

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

### <span data-ttu-id="a3cd1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3cd1-115">-Name</span></span>
<span data-ttu-id="a3cd1-116">O nome da conta dos serviços de mídia.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-116">The Media Services account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3cd1-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a3cd1-117">-Profile</span></span>
<span data-ttu-id="a3cd1-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a3cd1-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a3cd1-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3cd1-120">-Confirm</span></span>
<span data-ttu-id="a3cd1-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3cd1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3cd1-122">-WhatIf</span></span>
<span data-ttu-id="a3cd1-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3cd1-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3cd1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3cd1-125">CommonParameters</span></span>
<span data-ttu-id="a3cd1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3cd1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3cd1-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3cd1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3cd1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3cd1-128">INPUTS</span></span>

## <span data-ttu-id="a3cd1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3cd1-129">OUTPUTS</span></span>

## <span data-ttu-id="a3cd1-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3cd1-130">NOTES</span></span>

## <span data-ttu-id="a3cd1-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3cd1-131">RELATED LINKS</span></span>

[<span data-ttu-id="a3cd1-132">Como usar o Azure PowerShell para serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="a3cd1-132">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="a3cd1-133">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a3cd1-133">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="a3cd1-134">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a3cd1-134">New-AzureMediaServicesAccount</span></span>](./New-AzureMediaServicesAccount.md)


