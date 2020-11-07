---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D927B159-AD68-4071-ADE3-FA2430750D72
online version: ''
schema: 2.0.0
ms.openlocfilehash: 001466cb00ad15f1cbfef6dcf9fd3ce9b931109b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946455"
---
# <span data-ttu-id="4198f-101">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4198f-101">Remove-AzureStoreAddOn</span></span>

## <span data-ttu-id="4198f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4198f-102">SYNOPSIS</span></span>
<span data-ttu-id="4198f-103">Remove uma instância de complemento existente.</span><span class="sxs-lookup"><span data-stu-id="4198f-103">Removes an existing add-on instance.</span></span>

## <span data-ttu-id="4198f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4198f-104">SYNTAX</span></span>

```
Remove-AzureStoreAddOn -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4198f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4198f-105">DESCRIPTION</span></span>
<span data-ttu-id="4198f-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4198f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4198f-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4198f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4198f-108">Remove uma instância de complemento existente da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4198f-108">Removes an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="4198f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4198f-109">EXAMPLES</span></span>

### <span data-ttu-id="4198f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4198f-110">Example 1</span></span>
```
PS C:\> Remove-AzureStoreAddOn MyAddOn
```

<span data-ttu-id="4198f-111">Este exemplo remove um complemento chamado myaddon da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4198f-111">This example removes an add-on named MyAddOn from the current subscription.</span></span>

## <span data-ttu-id="4198f-112">OS</span><span class="sxs-lookup"><span data-stu-id="4198f-112">PARAMETERS</span></span>

### <span data-ttu-id="4198f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4198f-113">-Name</span></span>
<span data-ttu-id="4198f-114">Especifica o nome da instância do complemento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4198f-114">Specifies the name of the add-on instance to remove.</span></span>

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

### <span data-ttu-id="4198f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4198f-115">-PassThru</span></span>
<span data-ttu-id="4198f-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="4198f-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4198f-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4198f-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4198f-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4198f-118">-Profile</span></span>
<span data-ttu-id="4198f-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4198f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4198f-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4198f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4198f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4198f-121">CommonParameters</span></span>
<span data-ttu-id="4198f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4198f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4198f-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4198f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4198f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4198f-124">INPUTS</span></span>

## <span data-ttu-id="4198f-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4198f-125">OUTPUTS</span></span>

## <span data-ttu-id="4198f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4198f-126">NOTES</span></span>

## <span data-ttu-id="4198f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4198f-127">RELATED LINKS</span></span>

[<span data-ttu-id="4198f-128">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4198f-128">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="4198f-129">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4198f-129">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="4198f-130">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4198f-130">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


