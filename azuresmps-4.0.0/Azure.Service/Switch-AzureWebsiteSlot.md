---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 496ABC97-A493-4E42-B998-28A907DFBC19
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0641fd7bc8dcfa5048ac3e9d922bade199af2bab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945939"
---
# <span data-ttu-id="99cf7-101">Switch-AzureWebsiteSlot</span><span class="sxs-lookup"><span data-stu-id="99cf7-101">Switch-AzureWebsiteSlot</span></span>

## <span data-ttu-id="99cf7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="99cf7-103">Permuta o slot de produção para um site com outro slot.</span><span class="sxs-lookup"><span data-stu-id="99cf7-103">Swaps the production slot for a website with another slot.</span></span>

## <span data-ttu-id="99cf7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99cf7-104">SYNTAX</span></span>

```
Switch-AzureWebsiteSlot [-Name <String>] [-Slot1 <String>] [-Slot2 <String>] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99cf7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99cf7-105">DESCRIPTION</span></span>
<span data-ttu-id="99cf7-106">O cmdlet **switch-AzureWebsiteSlot** troca o slot de produção para um site com outro slot.</span><span class="sxs-lookup"><span data-stu-id="99cf7-106">The **Switch-AzureWebsiteSlot** cmdlet swaps the production slot for a website with another slot.</span></span>
<span data-ttu-id="99cf7-107">Isso funciona em sites com apenas dois slots.</span><span class="sxs-lookup"><span data-stu-id="99cf7-107">This works on websites with two slots only.</span></span>

## <span data-ttu-id="99cf7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99cf7-108">EXAMPLES</span></span>

### <span data-ttu-id="99cf7-109">Exemplo 1: trocar o slot do site</span><span class="sxs-lookup"><span data-stu-id="99cf7-109">Example 1: Switch Website Slot</span></span>
```
PS C:\> Switch-AzureWebsiteSlot -Name MyWebsite
```

<span data-ttu-id="99cf7-110">Alternar o slot de backup de mysite do site do Azure com o slot de produção.</span><span class="sxs-lookup"><span data-stu-id="99cf7-110">Switch the azure website MyWebsite backup slot with production slot.</span></span>

## <span data-ttu-id="99cf7-111">OS</span><span class="sxs-lookup"><span data-stu-id="99cf7-111">PARAMETERS</span></span>

### <span data-ttu-id="99cf7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="99cf7-112">-Force</span></span>
<span data-ttu-id="99cf7-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="99cf7-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99cf7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="99cf7-114">-Name</span></span>
<span data-ttu-id="99cf7-115">O nome do site.</span><span class="sxs-lookup"><span data-stu-id="99cf7-115">The name of the website.</span></span>

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

### <span data-ttu-id="99cf7-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="99cf7-116">-Profile</span></span>
<span data-ttu-id="99cf7-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="99cf7-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="99cf7-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="99cf7-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99cf7-119">-Slot1</span><span class="sxs-lookup"><span data-stu-id="99cf7-119">-Slot1</span></span>
<span data-ttu-id="99cf7-120">Especifica o primeiro slot.</span><span class="sxs-lookup"><span data-stu-id="99cf7-120">Specifies the first slot.</span></span>

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

### <span data-ttu-id="99cf7-121">-Slot2</span><span class="sxs-lookup"><span data-stu-id="99cf7-121">-Slot2</span></span>
<span data-ttu-id="99cf7-122">Especifica o segundo slot.</span><span class="sxs-lookup"><span data-stu-id="99cf7-122">Specifies the second slot.</span></span>

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

### <span data-ttu-id="99cf7-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="99cf7-123">-Confirm</span></span>
<span data-ttu-id="99cf7-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99cf7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99cf7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99cf7-125">-WhatIf</span></span>
<span data-ttu-id="99cf7-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99cf7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99cf7-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99cf7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99cf7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99cf7-128">CommonParameters</span></span>
<span data-ttu-id="99cf7-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99cf7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99cf7-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99cf7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99cf7-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99cf7-131">INPUTS</span></span>

## <span data-ttu-id="99cf7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99cf7-132">OUTPUTS</span></span>

## <span data-ttu-id="99cf7-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99cf7-133">NOTES</span></span>

## <span data-ttu-id="99cf7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99cf7-134">RELATED LINKS</span></span>

[<span data-ttu-id="99cf7-135">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="99cf7-135">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="99cf7-136">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="99cf7-136">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="99cf7-137">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="99cf7-137">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="99cf7-138">Parar-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="99cf7-138">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


