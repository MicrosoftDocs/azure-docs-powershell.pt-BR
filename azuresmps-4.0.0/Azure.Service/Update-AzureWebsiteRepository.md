---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: EFBC8DCD-00CC-4BBF-9383-EA15376535F3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42780f62bc68659874f7aae1e64ad5ce89038fdf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945843"
---
# <span data-ttu-id="7b590-101">Update-AzureWebsiteRepository</span><span class="sxs-lookup"><span data-stu-id="7b590-101">Update-AzureWebsiteRepository</span></span>

## <span data-ttu-id="7b590-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b590-102">SYNOPSIS</span></span>
<span data-ttu-id="7b590-103">Atualiza os repositórios remotos de um repositório git local para todos os slots.</span><span class="sxs-lookup"><span data-stu-id="7b590-103">Updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="7b590-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b590-104">SYNTAX</span></span>

```
Update-AzureWebsiteRepository [-Name <String>] -PublishingUsername <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b590-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b590-105">DESCRIPTION</span></span>
<span data-ttu-id="7b590-106">O cmdlet **Update-AzureWebsiteRepository** atualiza os repositórios remotos de um repositório git local para todos os slots.</span><span class="sxs-lookup"><span data-stu-id="7b590-106">The **Update-AzureWebsiteRepository** cmdlet updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="7b590-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b590-107">EXAMPLES</span></span>

### <span data-ttu-id="7b590-108">Exemplo 1: atualizar repositórios remotos do site</span><span class="sxs-lookup"><span data-stu-id="7b590-108">Example 1: Update Website Remote Repositories</span></span>
```
PS C:\> Update-AzureWebsiteRepository -Name MyWebsite
```

<span data-ttu-id="7b590-109">Atualiza os repositórios remotos de um repositório local do git para todos os slots do site mywebsite.</span><span class="sxs-lookup"><span data-stu-id="7b590-109">Updates the remote repositories of a local git repository for all the slots for website MyWebsite.</span></span>

## <span data-ttu-id="7b590-110">OS</span><span class="sxs-lookup"><span data-stu-id="7b590-110">PARAMETERS</span></span>

### <span data-ttu-id="7b590-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b590-111">-Name</span></span>
<span data-ttu-id="7b590-112">O nome do site.</span><span class="sxs-lookup"><span data-stu-id="7b590-112">The name of the website.</span></span>

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

### <span data-ttu-id="7b590-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7b590-113">-Profile</span></span>
<span data-ttu-id="7b590-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7b590-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7b590-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7b590-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7b590-116">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="7b590-116">-PublishingUsername</span></span>
<span data-ttu-id="7b590-117">O nome de usuário que você especificou no portal do Microsoft Azure para implantação do git.</span><span class="sxs-lookup"><span data-stu-id="7b590-117">The username you have specified in the Microsoft Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="7b590-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b590-118">-Confirm</span></span>
<span data-ttu-id="7b590-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b590-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b590-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b590-120">-WhatIf</span></span>
<span data-ttu-id="7b590-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b590-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b590-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b590-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b590-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b590-123">CommonParameters</span></span>
<span data-ttu-id="7b590-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b590-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b590-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b590-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b590-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b590-126">INPUTS</span></span>

## <span data-ttu-id="7b590-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b590-127">OUTPUTS</span></span>

## <span data-ttu-id="7b590-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b590-128">NOTES</span></span>

## <span data-ttu-id="7b590-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b590-129">RELATED LINKS</span></span>

[<span data-ttu-id="7b590-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7b590-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="7b590-131">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7b590-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="7b590-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7b590-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="7b590-133">Parar-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7b590-133">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


