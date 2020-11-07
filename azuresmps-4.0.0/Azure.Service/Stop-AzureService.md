---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 939A28A4-394A-4447-9EFA-8F2876D04DCD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b140c2c0efac81e361e2bab510cfeaf6210ef884
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945807"
---
# <span data-ttu-id="de188-101">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="de188-101">Stop-AzureService</span></span>

## <span data-ttu-id="de188-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de188-102">SYNOPSIS</span></span>
<span data-ttu-id="de188-103">Interrompe o serviço hospedado atual.</span><span class="sxs-lookup"><span data-stu-id="de188-103">Stops the current hosted service.</span></span>

## <span data-ttu-id="de188-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de188-104">SYNTAX</span></span>

```
Stop-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="de188-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de188-105">DESCRIPTION</span></span>
<span data-ttu-id="de188-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de188-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="de188-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="de188-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="de188-108">O cmdlet **Stop-AzureService** interrompe o serviço hospedado atual no slot especificado no Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="de188-108">The **Stop-AzureService** cmdlet stops the current hosted service in the specified slot in Windows Azure.</span></span>
<span data-ttu-id="de188-109">Se nenhum slot for especificado, o cmdlet para o serviço no slot de produção.</span><span class="sxs-lookup"><span data-stu-id="de188-109">If no slot is specified, the cmdlet stops the service in the Production slot.</span></span>

## <span data-ttu-id="de188-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de188-110">EXAMPLES</span></span>

## <span data-ttu-id="de188-111">OS</span><span class="sxs-lookup"><span data-stu-id="de188-111">PARAMETERS</span></span>

### <span data-ttu-id="de188-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de188-112">-PassThru</span></span>
<span data-ttu-id="de188-113">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="de188-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="de188-114">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="de188-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="de188-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="de188-115">-Profile</span></span>
<span data-ttu-id="de188-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="de188-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="de188-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="de188-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="de188-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="de188-118">-ServiceName</span></span>
<span data-ttu-id="de188-119">Especifica o nome do serviço hospedado para parar.</span><span class="sxs-lookup"><span data-stu-id="de188-119">Specifies the name of the hosted service to stop.</span></span>
<span data-ttu-id="de188-120">Se nenhum nome for especificado, o cmdlet para o serviço hospedado atual.</span><span class="sxs-lookup"><span data-stu-id="de188-120">If no name is specified, the cmdlet stops the current hosted service.</span></span>

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

### <span data-ttu-id="de188-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="de188-121">-Slot</span></span>
<span data-ttu-id="de188-122">Especifica o slot em que o serviço está hospedado, em preparação ou em produção.</span><span class="sxs-lookup"><span data-stu-id="de188-122">Specifies the slot where the service is hosted, either Staging or Production.</span></span>
<span data-ttu-id="de188-123">Se nenhum slot for especificado, a produção será presumida.</span><span class="sxs-lookup"><span data-stu-id="de188-123">If no slot is specified,  Production is assumed.</span></span>

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

### <span data-ttu-id="de188-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de188-124">CommonParameters</span></span>
<span data-ttu-id="de188-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de188-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de188-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de188-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de188-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de188-127">INPUTS</span></span>

## <span data-ttu-id="de188-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de188-128">OUTPUTS</span></span>

## <span data-ttu-id="de188-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de188-129">NOTES</span></span>

## <span data-ttu-id="de188-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de188-130">RELATED LINKS</span></span>

[<span data-ttu-id="de188-131">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="de188-131">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="de188-132">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="de188-132">Start-AzureService</span></span>](./Start-AzureService.md)


