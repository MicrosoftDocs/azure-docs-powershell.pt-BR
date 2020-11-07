---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DB3F85D6-5962-4288-AD75-0C30448B769C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88438fa66e39b5ad63db7b6d2609107d224f7faf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946020"
---
# <span data-ttu-id="5edb2-101">Unpublish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="5edb2-101">Unpublish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="5edb2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5edb2-102">SYNOPSIS</span></span>
<span data-ttu-id="5edb2-103">Cancela a publicação de um programa do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5edb2-103">Unpublishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="5edb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5edb2-104">SYNTAX</span></span>

```
Unpublish-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String[]>] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5edb2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5edb2-105">DESCRIPTION</span></span>
<span data-ttu-id="5edb2-106">O cmdlet **AzureRemoteAppProgram não publica** não publica um programa Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5edb2-106">The **Unpublish-AzureRemoteAppProgram** cmdlet unpublishes an Azure RemoteApp program.</span></span>
<span data-ttu-id="5edb2-107">Depois que você cancelar a publicação de um programa, ele não estará mais disponível para os usuários de uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5edb2-107">After you unpublish a program, it is no longer available to the users of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="5edb2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5edb2-108">EXAMPLES</span></span>

## <span data-ttu-id="5edb2-109">OS</span><span class="sxs-lookup"><span data-stu-id="5edb2-109">PARAMETERS</span></span>

### <span data-ttu-id="5edb2-110">-Alias</span><span class="sxs-lookup"><span data-stu-id="5edb2-110">-Alias</span></span>
<span data-ttu-id="5edb2-111">Especifica uma matriz de aliases dos programas a serem cancelados.</span><span class="sxs-lookup"><span data-stu-id="5edb2-111">Specifies an array of aliases of the programs to unpublish.</span></span>
<span data-ttu-id="5edb2-112">Use **Get-AzureRemoteAppProgram** para recuperar o alias de um programa para cancelar a publicação.</span><span class="sxs-lookup"><span data-stu-id="5edb2-112">Use **Get-AzureRemoteAppProgram** to retrieve the alias of a program to unpublish.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edb2-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="5edb2-113">-CollectionName</span></span>
<span data-ttu-id="5edb2-114">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5edb2-114">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edb2-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5edb2-115">-Profile</span></span>
<span data-ttu-id="5edb2-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5edb2-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5edb2-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5edb2-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5edb2-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5edb2-118">-Confirm</span></span>
<span data-ttu-id="5edb2-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5edb2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5edb2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5edb2-120">-WhatIf</span></span>
<span data-ttu-id="5edb2-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5edb2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5edb2-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5edb2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5edb2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edb2-123">CommonParameters</span></span>
<span data-ttu-id="5edb2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5edb2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edb2-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5edb2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edb2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5edb2-126">INPUTS</span></span>

## <span data-ttu-id="5edb2-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5edb2-127">OUTPUTS</span></span>

## <span data-ttu-id="5edb2-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5edb2-128">NOTES</span></span>

## <span data-ttu-id="5edb2-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5edb2-129">RELATED LINKS</span></span>

[<span data-ttu-id="5edb2-130">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="5edb2-130">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="5edb2-131">Publicar-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="5edb2-131">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)


