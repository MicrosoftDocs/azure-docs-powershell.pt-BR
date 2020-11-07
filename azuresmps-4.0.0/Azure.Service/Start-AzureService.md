---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 821CB3E4-102E-440A-8C92-D1890899A6EE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 64924d579eebb826bc9c36468da1617370f48cf7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946030"
---
# <span data-ttu-id="225c5-101">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="225c5-101">Start-AzureService</span></span>

## <span data-ttu-id="225c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="225c5-102">SYNOPSIS</span></span>
<span data-ttu-id="225c5-103">Inicia o serviço hospedado especificado no Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="225c5-103">Starts the specified hosted service in Windows Azure.</span></span>

## <span data-ttu-id="225c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="225c5-104">SYNTAX</span></span>

```
Start-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="225c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="225c5-105">DESCRIPTION</span></span>
<span data-ttu-id="225c5-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="225c5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="225c5-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="225c5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="225c5-108">O cmdlet **Start-AzureService** inicia o serviço hospedado especificado no Windows Azure, se o serviço estiver no estado parado.</span><span class="sxs-lookup"><span data-stu-id="225c5-108">The **Start-AzureService** cmdlet starts the specified hosted service in Windows Azure, if the service is in the stopped state.</span></span>
<span data-ttu-id="225c5-109">Observe que o cmdlet **Publish-AzureServiceProject** tenta iniciar automaticamente o serviço.</span><span class="sxs-lookup"><span data-stu-id="225c5-109">Note that the **Publish-AzureServiceProject** cmdlet automatically attempts to start the service.</span></span>

## <span data-ttu-id="225c5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="225c5-110">EXAMPLES</span></span>

## <span data-ttu-id="225c5-111">OS</span><span class="sxs-lookup"><span data-stu-id="225c5-111">PARAMETERS</span></span>

### <span data-ttu-id="225c5-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="225c5-112">-PassThru</span></span>
<span data-ttu-id="225c5-113">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="225c5-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="225c5-114">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="225c5-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="225c5-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="225c5-115">-Profile</span></span>
<span data-ttu-id="225c5-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="225c5-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="225c5-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="225c5-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="225c5-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="225c5-118">-ServiceName</span></span>
<span data-ttu-id="225c5-119">Especifica o nome do serviço hospedado a ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="225c5-119">Specifies the name of the hosted service to start.</span></span>
<span data-ttu-id="225c5-120">Se não for especificado um nome, o cmdlet iniciará o serviço hospedado atual.</span><span class="sxs-lookup"><span data-stu-id="225c5-120">If no name is specified, the cmdlet starts the current hosted service.</span></span>

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

### <span data-ttu-id="225c5-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="225c5-121">-Slot</span></span>
<span data-ttu-id="225c5-122">Especifica o slot de implantação no qual iniciar o serviço, seja para transferência ou produção.</span><span class="sxs-lookup"><span data-stu-id="225c5-122">Specifies the deployment slot in which to start the service, either Staging or Production.</span></span>

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

### <span data-ttu-id="225c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225c5-123">CommonParameters</span></span>
<span data-ttu-id="225c5-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="225c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225c5-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225c5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225c5-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="225c5-126">INPUTS</span></span>

## <span data-ttu-id="225c5-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="225c5-127">OUTPUTS</span></span>

## <span data-ttu-id="225c5-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="225c5-128">NOTES</span></span>

## <span data-ttu-id="225c5-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="225c5-129">RELATED LINKS</span></span>

[<span data-ttu-id="225c5-130">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="225c5-130">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="225c5-131">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="225c5-131">Start-AzureService</span></span>](./Start-AzureService.md)

[<span data-ttu-id="225c5-132">Parar-AzureService</span><span class="sxs-lookup"><span data-stu-id="225c5-132">Stop-AzureService</span></span>](./Stop-AzureService.md)


