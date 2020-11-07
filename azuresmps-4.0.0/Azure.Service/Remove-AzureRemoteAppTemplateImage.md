---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946149"
---
# <span data-ttu-id="e9f6d-101">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e9f6d-101">Remove-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="e9f6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f6d-103">Exclui uma imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-103">Deletes an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="e9f6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9f6d-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9f6d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9f6d-105">DESCRIPTION</span></span>
<span data-ttu-id="e9f6d-106">O cmdlet **Remove-AzureRemoteAppTemplateImage** exclui uma imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-106">The **Remove-AzureRemoteAppTemplateImage** cmdlet deletes an Azure RemoteApp template image.</span></span>
<span data-ttu-id="e9f6d-107">Uma imagem de modelo só poderá ser excluída se não estiver vinculada a nenhuma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-107">A template image can deleted only if it is not linked to any Azure RemoteApp collection.</span></span>

## <span data-ttu-id="e9f6d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9f6d-108">EXAMPLES</span></span>

### <span data-ttu-id="e9f6d-109">Exemplo 1: excluir uma imagem de modelo</span><span class="sxs-lookup"><span data-stu-id="e9f6d-109">Example 1: Delete a template image</span></span>
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="e9f6d-110">Esse comando exclui a imagem de modelo chamada ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-110">This command deletes the template image named ContosoApps.</span></span>

## <span data-ttu-id="e9f6d-111">OS</span><span class="sxs-lookup"><span data-stu-id="e9f6d-111">PARAMETERS</span></span>

### <span data-ttu-id="e9f6d-112">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e9f6d-112">-ImageName</span></span>
<span data-ttu-id="e9f6d-113">Especifica o nome da imagem de modelo do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-113">Specifies the name of the RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f6d-114">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e9f6d-114">-Profile</span></span>
<span data-ttu-id="e9f6d-115">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9f6d-116">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9f6d-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e9f6d-117">-Confirm</span></span>
<span data-ttu-id="e9f6d-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f6d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f6d-119">-WhatIf</span></span>
<span data-ttu-id="e9f6d-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9f6d-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f6d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f6d-122">CommonParameters</span></span>
<span data-ttu-id="e9f6d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f6d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f6d-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f6d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f6d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9f6d-125">INPUTS</span></span>

## <span data-ttu-id="e9f6d-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9f6d-126">OUTPUTS</span></span>

## <span data-ttu-id="e9f6d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9f6d-127">NOTES</span></span>

## <span data-ttu-id="e9f6d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9f6d-128">RELATED LINKS</span></span>

[<span data-ttu-id="e9f6d-129">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e9f6d-129">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="e9f6d-130">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e9f6d-130">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="e9f6d-131">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e9f6d-131">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


