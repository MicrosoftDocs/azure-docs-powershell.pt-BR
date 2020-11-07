---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945819"
---
# <span data-ttu-id="3a221-101">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="3a221-101">Set-AzureServiceProject</span></span>

## <span data-ttu-id="3a221-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a221-102">SYNOPSIS</span></span>
<span data-ttu-id="3a221-103">Define a localização, a assinatura, o slot e a conta de armazenamento padrão para o serviço atual.</span><span class="sxs-lookup"><span data-stu-id="3a221-103">Sets default location, subscription, slot, and storage account for the current service.</span></span>

## <span data-ttu-id="3a221-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a221-104">SYNTAX</span></span>

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a221-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a221-105">DESCRIPTION</span></span>
<span data-ttu-id="3a221-106">O cmdlet **set-AzureServiceProject** define o local de implantação, o slot, a conta de armazenamento e a assinatura do serviço atual.</span><span class="sxs-lookup"><span data-stu-id="3a221-106">The **Set-AzureServiceProject** cmdlet sets the deployment location, slot, storage account, and subscription for the current service.</span></span>
<span data-ttu-id="3a221-107">Esses valores são usados sempre que o serviço é publicado na nuvem.</span><span class="sxs-lookup"><span data-stu-id="3a221-107">These values are used whenever the service is published to the cloud.</span></span>

## <span data-ttu-id="3a221-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a221-108">EXAMPLES</span></span>

### <span data-ttu-id="3a221-109">Exemplo 1: configurações básicas</span><span class="sxs-lookup"><span data-stu-id="3a221-109">Example 1: Basic settings</span></span>
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

<span data-ttu-id="3a221-110">Define o local de implantação do serviço para a região norte central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="3a221-110">Sets the deployment location for the service to the North Central US region.</span></span>
<span data-ttu-id="3a221-111">Define o slot de implantação como produção.</span><span class="sxs-lookup"><span data-stu-id="3a221-111">Sets the deployment slot to Production.</span></span> <span data-ttu-id="3a221-112">Define a conta de armazenamento que será usada para testar a definição do serviço para myStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="3a221-112">Sets the storage account that will be used to stage the service definition to myStorageAccount.</span></span>
<span data-ttu-id="3a221-113">Define a assinatura que hospedará o serviço para a minha assinatura.</span><span class="sxs-lookup"><span data-stu-id="3a221-113">Sets the subscription that will host the service to mySubscription.</span></span>
<span data-ttu-id="3a221-114">Sempre que o serviço for publicado na nuvem, ele será hospedado em um Data Center na região do Norte Central dos EUA, ele atualizará o slot de implantação e usará a assinatura especificada e a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a221-114">Whenever the service is published to the cloud, it will be hosted in a data center in the North Central US region, it will update the deployment slot, and it will use the specified subscription and storage account.</span></span>

## <span data-ttu-id="3a221-115">OS</span><span class="sxs-lookup"><span data-stu-id="3a221-115">PARAMETERS</span></span>

### <span data-ttu-id="3a221-116">-Local</span><span class="sxs-lookup"><span data-stu-id="3a221-116">-Location</span></span>
<span data-ttu-id="3a221-117">A região em que o serviço será hospedado.</span><span class="sxs-lookup"><span data-stu-id="3a221-117">The region in which the service will be hosted.</span></span>
<span data-ttu-id="3a221-118">Esse valor é usado sempre que o serviço for publicado na nuvem.</span><span class="sxs-lookup"><span data-stu-id="3a221-118">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="3a221-119">Os valores possíveis são: em qualquer lugar da Ásia, em qualquer lugar da Europa, em qualquer lugar, na Ásia Oriental, no leste dos EUA, centro-norte da América do Sul, centro-oeste dos EUA, Sudeste Asiático, West Europe, West US.</span><span class="sxs-lookup"><span data-stu-id="3a221-119">Possible values are: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span></span>

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

### <span data-ttu-id="3a221-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a221-120">-PassThru</span></span>
<span data-ttu-id="3a221-121">Indica que esse cmdlet retorna um objeto que representa o item no qual ele funciona.</span><span class="sxs-lookup"><span data-stu-id="3a221-121">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="3a221-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3a221-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a221-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3a221-123">-Profile</span></span>
<span data-ttu-id="3a221-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3a221-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a221-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3a221-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a221-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="3a221-126">-Slot</span></span>
<span data-ttu-id="3a221-127">O slot (produção ou preparação) em que o serviço será hospedado.</span><span class="sxs-lookup"><span data-stu-id="3a221-127">The slot (production or staging) in which the service will be hosted.</span></span>
<span data-ttu-id="3a221-128">Esse valor é usado sempre que o serviço for publicado na nuvem.</span><span class="sxs-lookup"><span data-stu-id="3a221-128">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="3a221-129">Os valores possíveis são: produção, preparação.</span><span class="sxs-lookup"><span data-stu-id="3a221-129">Possible values are: Production, Staging.</span></span>

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

### <span data-ttu-id="3a221-130">-Armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a221-130">-Storage</span></span>
<span data-ttu-id="3a221-131">A conta de armazenamento a ser usada ao carregar o pacote de serviço para a nuvem.</span><span class="sxs-lookup"><span data-stu-id="3a221-131">The storage account to be used when uploading the service package to the cloud.</span></span>
<span data-ttu-id="3a221-132">Se a conta de armazenamento não existir, ela será criada quando o serviço for publicado na nuvem.</span><span class="sxs-lookup"><span data-stu-id="3a221-132">If the storage account doesn't exist, it will be created when the service is published to the cloud.</span></span>

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

### <span data-ttu-id="3a221-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a221-133">CommonParameters</span></span>
<span data-ttu-id="3a221-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a221-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a221-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a221-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a221-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a221-136">INPUTS</span></span>

## <span data-ttu-id="3a221-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a221-137">OUTPUTS</span></span>

## <span data-ttu-id="3a221-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a221-138">NOTES</span></span>
* <span data-ttu-id="3a221-139">nó-dev, php-dev, Python-dev</span><span class="sxs-lookup"><span data-stu-id="3a221-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="3a221-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a221-140">RELATED LINKS</span></span>

[<span data-ttu-id="3a221-141">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="3a221-141">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="3a221-142">Publicar-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="3a221-142">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="3a221-143">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="3a221-143">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


