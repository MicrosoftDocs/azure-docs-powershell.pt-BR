---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B107D789-8F66-4D7D-B126-08ACB0364826
online version: ''
schema: 2.0.0
ms.openlocfilehash: e59df078539e9ea94073defd4c8ea13a69cc2e5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945487"
---
# <span data-ttu-id="3b626-101">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="3b626-101">Remove-AzureVirtualIP</span></span>

## <span data-ttu-id="3b626-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b626-102">SYNOPSIS</span></span>
<span data-ttu-id="3b626-103">Exclui um endereço IP virtual de seu serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="3b626-103">Deletes a virtual IP address from your Cloud Service.</span></span>

## <span data-ttu-id="3b626-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b626-104">SYNTAX</span></span>

```
Remove-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3b626-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b626-105">DESCRIPTION</span></span>
<span data-ttu-id="3b626-106">O cmdlet **Remove-AzureVirtualIP** exclui um VIP (IP virtual) de um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b626-106">The **Remove-AzureVirtualIP** cmdlet deletes a virtual IP (VIP) from an Azure service.</span></span>
<span data-ttu-id="3b626-107">A operação será bem-sucedida apenas se o IP virtual não tiver pontos de extremidade associados a ele.</span><span class="sxs-lookup"><span data-stu-id="3b626-107">The operation succeeds only if the virtual IP has no endpoints associated with it.</span></span>

## <span data-ttu-id="3b626-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b626-108">EXAMPLES</span></span>

### <span data-ttu-id="3b626-109">Exemplo 1: remover um endereço IP virtual de um serviço</span><span class="sxs-lookup"><span data-stu-id="3b626-109">Example 1: Remove a virtual IP address from a service</span></span>
```
PS C:\> Remove-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
```

<span data-ttu-id="3b626-110">Esse comando Remove um endereço IP virtual de um serviço.</span><span class="sxs-lookup"><span data-stu-id="3b626-110">This command removes a virtual IP address from a service.</span></span>

## <span data-ttu-id="3b626-111">OS</span><span class="sxs-lookup"><span data-stu-id="3b626-111">PARAMETERS</span></span>

### <span data-ttu-id="3b626-112">-Force</span><span class="sxs-lookup"><span data-stu-id="3b626-112">-Force</span></span>
<span data-ttu-id="3b626-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b626-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b626-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="3b626-114">-InformationAction</span></span>
<span data-ttu-id="3b626-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="3b626-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3b626-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3b626-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b626-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="3b626-117">Continue</span></span>
- <span data-ttu-id="3b626-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="3b626-118">Ignore</span></span>
- <span data-ttu-id="3b626-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="3b626-119">Inquire</span></span>
- <span data-ttu-id="3b626-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3b626-120">SilentlyContinue</span></span>
- <span data-ttu-id="3b626-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="3b626-121">Stop</span></span>
- <span data-ttu-id="3b626-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="3b626-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b626-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3b626-123">-InformationVariable</span></span>
<span data-ttu-id="3b626-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="3b626-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b626-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3b626-125">-Profile</span></span>
<span data-ttu-id="3b626-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3b626-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b626-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3b626-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b626-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3b626-128">-ServiceName</span></span>
<span data-ttu-id="3b626-129">Especifica o nome do serviço do qual você deseja remover um endereço IP virtual.</span><span class="sxs-lookup"><span data-stu-id="3b626-129">Specifies the name of the service from which to remove a virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b626-130">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="3b626-130">-VirtualIPName</span></span>
<span data-ttu-id="3b626-131">Especifica o nome do endereço IP virtual a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3b626-131">Specifies the name of the virtual IP address to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b626-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b626-132">CommonParameters</span></span>
<span data-ttu-id="3b626-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b626-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b626-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b626-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b626-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b626-135">INPUTS</span></span>

## <span data-ttu-id="3b626-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b626-136">OUTPUTS</span></span>

### <span data-ttu-id="3b626-137">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="3b626-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="3b626-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b626-138">NOTES</span></span>

## <span data-ttu-id="3b626-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b626-139">RELATED LINKS</span></span>

[<span data-ttu-id="3b626-140">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="3b626-140">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)


