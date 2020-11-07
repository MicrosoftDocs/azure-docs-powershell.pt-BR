---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6E369BDF-AE3C-416B-81B7-097C20147CBE
online version: ''
schema: 2.0.0
ms.openlocfilehash: bb48f7412c957ceefb7df03d79e57ce8e75447d5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946130"
---
# <span data-ttu-id="337dd-101">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="337dd-101">Remove-AzureSBNamespace</span></span>

## <span data-ttu-id="337dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="337dd-102">SYNOPSIS</span></span>
<span data-ttu-id="337dd-103">Remove um namespace.</span><span class="sxs-lookup"><span data-stu-id="337dd-103">Removes a namespace.</span></span>

## <span data-ttu-id="337dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="337dd-104">SYNTAX</span></span>

```
Remove-AzureSBNamespace -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="337dd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="337dd-105">DESCRIPTION</span></span>
<span data-ttu-id="337dd-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="337dd-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="337dd-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="337dd-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="337dd-108">O cmdlet **Remove-AzureSBNamespace** remove um namespace de serviço para o barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="337dd-108">The **Remove-AzureSBNamespace** cmdlet removes a service namespace for Service Bus.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="337dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="337dd-109">EXAMPLES</span></span>

## <span data-ttu-id="337dd-110">OS</span><span class="sxs-lookup"><span data-stu-id="337dd-110">PARAMETERS</span></span>

### <span data-ttu-id="337dd-111">-Force</span><span class="sxs-lookup"><span data-stu-id="337dd-111">-Force</span></span>
<span data-ttu-id="337dd-112">Se habilitado, remove o namespace sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="337dd-112">If enabled, removes the namespace without prompting for confirmation.</span></span>

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

### <span data-ttu-id="337dd-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="337dd-113">-Name</span></span>
<span data-ttu-id="337dd-114">Especifica o nome do namespace a ser removido.</span><span class="sxs-lookup"><span data-stu-id="337dd-114">Specifies the name of the namespace to be removed.</span></span>

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

### <span data-ttu-id="337dd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="337dd-115">-PassThru</span></span>
<span data-ttu-id="337dd-116">Faz com que a operação retorne true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="337dd-116">Causes the operation to return true if it succeeds.</span></span>

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

### <span data-ttu-id="337dd-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="337dd-117">-Profile</span></span>
<span data-ttu-id="337dd-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="337dd-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="337dd-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="337dd-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="337dd-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="337dd-120">-Confirm</span></span>
<span data-ttu-id="337dd-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="337dd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="337dd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="337dd-122">-WhatIf</span></span>
<span data-ttu-id="337dd-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="337dd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="337dd-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="337dd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="337dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337dd-125">CommonParameters</span></span>
<span data-ttu-id="337dd-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="337dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337dd-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="337dd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337dd-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="337dd-128">INPUTS</span></span>

## <span data-ttu-id="337dd-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="337dd-129">OUTPUTS</span></span>

## <span data-ttu-id="337dd-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="337dd-130">NOTES</span></span>

## <span data-ttu-id="337dd-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="337dd-131">RELATED LINKS</span></span>

[<span data-ttu-id="337dd-132">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="337dd-132">New-AzureSBNamespace</span></span>](./New-AzureSBNamespace.md)


