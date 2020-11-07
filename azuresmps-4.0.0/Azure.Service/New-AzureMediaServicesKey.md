---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 756F757C-8CDE-43A5-A8A6-D55EF9C66183
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71402e56251e2632c73a9185a1e70b4e3de8d770
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946001"
---
# <span data-ttu-id="9b9aa-101">New-AzureMediaServicesKey</span><span class="sxs-lookup"><span data-stu-id="9b9aa-101">New-AzureMediaServicesKey</span></span>

## <span data-ttu-id="9b9aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b9aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9b9aa-103">Atualiza as chaves de conta do Azure Media Services.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-103">Updates Azure Media Services account keys.</span></span>

<span data-ttu-id="9b9aa-104">**Observação:** Esta versão foi preterida, confira a [versão mais recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="9b9aa-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="9b9aa-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b9aa-105">SYNTAX</span></span>

```
New-AzureMediaServicesKey -Name <String> -KeyType <MediaServicesKeyType> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b9aa-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b9aa-106">DESCRIPTION</span></span>
<span data-ttu-id="9b9aa-107">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9b9aa-108">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9b9aa-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9b9aa-109">O cmdlet **New-AzureMediaServicesKey** atualiza a chave primária ou secundária para a conta de serviços de mídia especificada.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-109">The **New-AzureMediaServicesKey** cmdlet updates the Primary or Secondary key for the specified Media Services account.</span></span>

## <span data-ttu-id="9b9aa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b9aa-110">EXAMPLES</span></span>

### <span data-ttu-id="9b9aa-111">Exemplo 1: atualizar uma chave de conta do Media Services</span><span class="sxs-lookup"><span data-stu-id="9b9aa-111">Example 1: Update a Media Services account key</span></span>
```
PS C:\> New-AzureMediaServicesKey -Name "mediaservicesaccount" -KeyType "Primary" -Force
```

## <span data-ttu-id="9b9aa-112">OS</span><span class="sxs-lookup"><span data-stu-id="9b9aa-112">PARAMETERS</span></span>

### <span data-ttu-id="9b9aa-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9b9aa-113">-Force</span></span>
<span data-ttu-id="9b9aa-114">Indica que a geração de chave não está confirmada.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-114">Indicates that the key generation is not confirmed.</span></span>

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

### <span data-ttu-id="9b9aa-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="9b9aa-115">-KeyType</span></span>
<span data-ttu-id="9b9aa-116">Especifica o tipo de chave do serviços de mídia; Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9b9aa-116">Specifies the Media Services key type; Valid values are:</span></span>
  
- <span data-ttu-id="9b9aa-117">Preocupação</span><span class="sxs-lookup"><span data-stu-id="9b9aa-117">Primary</span></span>
- <span data-ttu-id="9b9aa-118">Segundo</span><span class="sxs-lookup"><span data-stu-id="9b9aa-118">Secondary</span></span>

```yaml
Type: MediaServicesKeyType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b9aa-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b9aa-119">-Name</span></span>
<span data-ttu-id="9b9aa-120">Especifica o nome da conta de serviços de mídia.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-120">Specifies the name of the Media Services account.</span></span>

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

### <span data-ttu-id="9b9aa-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9b9aa-121">-Profile</span></span>
<span data-ttu-id="9b9aa-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b9aa-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9b9aa-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b9aa-124">-Confirm</span></span>
<span data-ttu-id="9b9aa-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b9aa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b9aa-126">-WhatIf</span></span>
<span data-ttu-id="9b9aa-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b9aa-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b9aa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b9aa-129">CommonParameters</span></span>
<span data-ttu-id="9b9aa-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b9aa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b9aa-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b9aa-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b9aa-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b9aa-132">INPUTS</span></span>

## <span data-ttu-id="9b9aa-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b9aa-133">OUTPUTS</span></span>

## <span data-ttu-id="9b9aa-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b9aa-134">NOTES</span></span>

## <span data-ttu-id="9b9aa-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b9aa-135">RELATED LINKS</span></span>

[<span data-ttu-id="9b9aa-136">Como usar o Azure PowerShell para serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="9b9aa-136">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


