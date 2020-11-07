---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7E1A3988-CEEA-49E1-B6F4-1EFA39E170C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06cc64eb67f1e338ff5be28712d1c183bfefd5ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946588"
---
# <span data-ttu-id="5240e-101">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5240e-101">Stop-AzureWebsite</span></span>

## <span data-ttu-id="5240e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5240e-102">SYNOPSIS</span></span>
<span data-ttu-id="5240e-103">Para o site especificado.</span><span class="sxs-lookup"><span data-stu-id="5240e-103">Stops the specified website.</span></span>

## <span data-ttu-id="5240e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5240e-104">SYNTAX</span></span>

```
Stop-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5240e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5240e-105">DESCRIPTION</span></span>
<span data-ttu-id="5240e-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5240e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5240e-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5240e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5240e-108">O cmdlet **Stop-AzureWebsite** interrompe o site especificado hospedado no Azure.</span><span class="sxs-lookup"><span data-stu-id="5240e-108">The **Stop-AzureWebsite** cmdlet stops the specified website hosted in Azure.</span></span>

## <span data-ttu-id="5240e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5240e-109">EXAMPLES</span></span>

## <span data-ttu-id="5240e-110">OS</span><span class="sxs-lookup"><span data-stu-id="5240e-110">PARAMETERS</span></span>

### <span data-ttu-id="5240e-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="5240e-111">-Name</span></span>
<span data-ttu-id="5240e-112">Especifica o nome do site para parar.</span><span class="sxs-lookup"><span data-stu-id="5240e-112">Specifies the name of the website to stop.</span></span>

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

### <span data-ttu-id="5240e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5240e-113">-PassThru</span></span>
<span data-ttu-id="5240e-114">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="5240e-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5240e-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5240e-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5240e-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5240e-116">-Profile</span></span>
<span data-ttu-id="5240e-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5240e-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5240e-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5240e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5240e-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="5240e-119">-Slot</span></span>
<span data-ttu-id="5240e-120">Especifica o nome do slot do site.</span><span class="sxs-lookup"><span data-stu-id="5240e-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="5240e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5240e-121">CommonParameters</span></span>
<span data-ttu-id="5240e-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5240e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5240e-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5240e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5240e-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5240e-124">INPUTS</span></span>

## <span data-ttu-id="5240e-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5240e-125">OUTPUTS</span></span>

## <span data-ttu-id="5240e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5240e-126">NOTES</span></span>

## <span data-ttu-id="5240e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5240e-127">RELATED LINKS</span></span>

[<span data-ttu-id="5240e-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5240e-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="5240e-129">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5240e-129">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


