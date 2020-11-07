---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7F6EEF0-8896-4639-89A8-810F19161211
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b32c031a91adc3ab56e06898a1aa8ad70ac4e8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945470"
---
# <span data-ttu-id="de720-101">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="de720-101">Restart-AzureWebsite</span></span>

## <span data-ttu-id="de720-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de720-102">SYNOPSIS</span></span>
<span data-ttu-id="de720-103">Para e reinicia o site especificado.</span><span class="sxs-lookup"><span data-stu-id="de720-103">Stops and then restarts the specified website.</span></span>

## <span data-ttu-id="de720-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de720-104">SYNTAX</span></span>

```
Restart-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="de720-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de720-105">DESCRIPTION</span></span>
<span data-ttu-id="de720-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de720-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="de720-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="de720-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="de720-108">O cmdlet **Restart-AzureWebsite** interrompe e, em seguida, reinicia o site especificado.</span><span class="sxs-lookup"><span data-stu-id="de720-108">The **Restart-AzureWebsite** cmdlet stops and then restarts the specified website.</span></span>

## <span data-ttu-id="de720-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de720-109">EXAMPLES</span></span>

### <span data-ttu-id="de720-110">Exemplo 1: reiniciar um site</span><span class="sxs-lookup"><span data-stu-id="de720-110">Example 1: Restart a website</span></span>
```
PS C:\> Restart-AzureWebsite -Name MyWebsite
```

<span data-ttu-id="de720-111">Este exemplo reinicia um site denominado mywebsite.</span><span class="sxs-lookup"><span data-stu-id="de720-111">This example restarts a website named MyWebsite.</span></span>

## <span data-ttu-id="de720-112">OS</span><span class="sxs-lookup"><span data-stu-id="de720-112">PARAMETERS</span></span>

### <span data-ttu-id="de720-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="de720-113">-Name</span></span>
<span data-ttu-id="de720-114">Especifica o nome do site do Azure a ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="de720-114">Specifies the name of the Azure website to restart.</span></span>

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

### <span data-ttu-id="de720-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de720-115">-PassThru</span></span>
<span data-ttu-id="de720-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="de720-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="de720-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="de720-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="de720-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="de720-118">-Profile</span></span>
<span data-ttu-id="de720-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="de720-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="de720-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="de720-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="de720-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="de720-121">-Slot</span></span>
<span data-ttu-id="de720-122">Especifica o nome do slot do site.</span><span class="sxs-lookup"><span data-stu-id="de720-122">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="de720-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de720-123">CommonParameters</span></span>
<span data-ttu-id="de720-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de720-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de720-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de720-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de720-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de720-126">INPUTS</span></span>

## <span data-ttu-id="de720-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de720-127">OUTPUTS</span></span>

## <span data-ttu-id="de720-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de720-128">NOTES</span></span>

## <span data-ttu-id="de720-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de720-129">RELATED LINKS</span></span>

[<span data-ttu-id="de720-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="de720-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="de720-131">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="de720-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="de720-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="de720-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="de720-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="de720-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


