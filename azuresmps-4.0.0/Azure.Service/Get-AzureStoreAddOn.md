---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945547"
---
# <span data-ttu-id="9ca99-101">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="9ca99-101">Get-AzureStoreAddOn</span></span>

## <span data-ttu-id="9ca99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ca99-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca99-103">Obtém os complementos disponíveis da loja do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca99-103">Gets the available Azure Store add-ons.</span></span>

## <span data-ttu-id="9ca99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ca99-104">SYNTAX</span></span>

### <span data-ttu-id="9ca99-105">ListAvailable</span><span class="sxs-lookup"><span data-stu-id="9ca99-105">ListAvailable</span></span>
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ca99-106">Getaddon</span><span class="sxs-lookup"><span data-stu-id="9ca99-106">GetAddOn</span></span>
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9ca99-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ca99-107">DESCRIPTION</span></span>
<span data-ttu-id="9ca99-108">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ca99-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9ca99-109">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9ca99-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9ca99-110">Obtém todos os complementos disponíveis para compra na loja do Azure ou obtém as instâncias de complemento existentes para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9ca99-110">Gets all the available add-ons for purchasing from the Azure Store, or gets the existing add-on instances for the current subscription.</span></span>

## <span data-ttu-id="9ca99-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ca99-111">EXAMPLES</span></span>

### <span data-ttu-id="9ca99-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ca99-112">Example 1</span></span>
```
PS C:\> Get-AzureStoreAddOn
```

<span data-ttu-id="9ca99-113">Este exemplo obtém todas as instâncias de complemento adquiridas para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9ca99-113">This example gets all purchased add-on instances for the current subscription.</span></span>

### <span data-ttu-id="9ca99-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9ca99-114">Example 2</span></span>
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

<span data-ttu-id="9ca99-115">Este exemplo obtém todos os complementos disponíveis para compras nos Estados Unidos na loja do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca99-115">This example gets all the available add-ons for purchasing in United States from the Azure Store.</span></span>

### <span data-ttu-id="9ca99-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9ca99-116">Example 3</span></span>
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

<span data-ttu-id="9ca99-117">Este exemplo obtém um complemento chamado myaddon da instância do complemento comprado na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9ca99-117">This example gets an add-on named MyAddOn from the purchased add-on instance in the current subscription.</span></span>

## <span data-ttu-id="9ca99-118">OS</span><span class="sxs-lookup"><span data-stu-id="9ca99-118">PARAMETERS</span></span>

### <span data-ttu-id="9ca99-119">-País</span><span class="sxs-lookup"><span data-stu-id="9ca99-119">-Country</span></span>
<span data-ttu-id="9ca99-120">Se especificado, retorna apenas as instâncias de complemento do Azure Store disponíveis no país especificado.</span><span class="sxs-lookup"><span data-stu-id="9ca99-120">If specified, returns only the Azure Store add-on instances available in the specified country.</span></span>
<span data-ttu-id="9ca99-121">O padrão é "US".</span><span class="sxs-lookup"><span data-stu-id="9ca99-121">The default is "US".</span></span>

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca99-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="9ca99-122">-ListAvailable</span></span>
<span data-ttu-id="9ca99-123">Se especificado, obtém Complementos disponíveis para compras na Azure Store.</span><span class="sxs-lookup"><span data-stu-id="9ca99-123">If specified, gets available add-ons for purchasing from the Azure Store.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca99-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ca99-124">-Name</span></span>
<span data-ttu-id="9ca99-125">Retorna o complemento que corresponde ao nome especificado.</span><span class="sxs-lookup"><span data-stu-id="9ca99-125">Returns the add-on that matches the specified name.</span></span>

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca99-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9ca99-126">-Profile</span></span>
<span data-ttu-id="9ca99-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9ca99-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9ca99-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9ca99-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9ca99-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca99-129">CommonParameters</span></span>
<span data-ttu-id="9ca99-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ca99-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca99-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ca99-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca99-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ca99-132">INPUTS</span></span>

## <span data-ttu-id="9ca99-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ca99-133">OUTPUTS</span></span>

## <span data-ttu-id="9ca99-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ca99-134">NOTES</span></span>

## <span data-ttu-id="9ca99-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ca99-135">RELATED LINKS</span></span>

[<span data-ttu-id="9ca99-136">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="9ca99-136">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="9ca99-137">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="9ca99-137">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="9ca99-138">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="9ca99-138">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


