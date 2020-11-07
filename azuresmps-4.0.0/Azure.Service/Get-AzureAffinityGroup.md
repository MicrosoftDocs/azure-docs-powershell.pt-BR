---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 77B26360-F22B-457F-BDE3-9920A5736947
online version: ''
schema: 2.0.0
ms.openlocfilehash: 323b04a57cffc71059dff3f91480d54684941695
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945671"
---
# <span data-ttu-id="131c7-101">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="131c7-101">Get-AzureAffinityGroup</span></span>

## <span data-ttu-id="131c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="131c7-102">SYNOPSIS</span></span>
<span data-ttu-id="131c7-103">Obtém um objeto do grupo de afinidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="131c7-103">Gets an Azure affinity group object.</span></span>

## <span data-ttu-id="131c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="131c7-104">SYNTAX</span></span>

```
Get-AzureAffinityGroup [[-Name] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="131c7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="131c7-105">DESCRIPTION</span></span>
<span data-ttu-id="131c7-106">O cmdlet **Get-AzureAffinityGroup** Obtém um grupo de afinidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="131c7-106">The **Get-AzureAffinityGroup** cmdlet gets an Azure affinity group.</span></span>
<span data-ttu-id="131c7-107">O objeto de grupo Affinity inclui o nome, o local, o rótulo, a descrição e o armazenamento e os serviços hospedados do grupo de afinidade que fazem parte do grupo de afinidade.</span><span class="sxs-lookup"><span data-stu-id="131c7-107">The affinity group object includes the affinity group name, location, label, description and the storage and hosted services that are part of the affinity group.</span></span>

## <span data-ttu-id="131c7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="131c7-108">EXAMPLES</span></span>

### <span data-ttu-id="131c7-109">Exemplo 1: obter propriedades de um grupo de afinidade</span><span class="sxs-lookup"><span data-stu-id="131c7-109">Example 1: Get properties of an affinity group</span></span>
```
PS C:\> Get-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="131c7-110">Esse comando obtém as propriedades do grupo de afinidade chamado South01.</span><span class="sxs-lookup"><span data-stu-id="131c7-110">This command gets the properties of the affinity group named South01.</span></span>

## <span data-ttu-id="131c7-111">OS</span><span class="sxs-lookup"><span data-stu-id="131c7-111">PARAMETERS</span></span>

### <span data-ttu-id="131c7-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="131c7-112">-InformationAction</span></span>
<span data-ttu-id="131c7-113">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="131c7-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="131c7-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="131c7-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="131c7-115">Contínuo</span><span class="sxs-lookup"><span data-stu-id="131c7-115">Continue</span></span>
- <span data-ttu-id="131c7-116">Ignorar</span><span class="sxs-lookup"><span data-stu-id="131c7-116">Ignore</span></span>
- <span data-ttu-id="131c7-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="131c7-117">Inquire</span></span>
- <span data-ttu-id="131c7-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="131c7-118">SilentlyContinue</span></span>
- <span data-ttu-id="131c7-119">Finaliza</span><span class="sxs-lookup"><span data-stu-id="131c7-119">Stop</span></span>
- <span data-ttu-id="131c7-120">Suspensão</span><span class="sxs-lookup"><span data-stu-id="131c7-120">Suspend</span></span>

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

### <span data-ttu-id="131c7-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="131c7-121">-InformationVariable</span></span>
<span data-ttu-id="131c7-122">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="131c7-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="131c7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="131c7-123">-Name</span></span>
<span data-ttu-id="131c7-124">Especifica o nome do grupo de afinidade que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="131c7-124">Specifies the name of the affinity group that this cmdlet gets.</span></span>
<span data-ttu-id="131c7-125">Os nomes para grupos de afinidade criados por meio do portal de gerenciamento geralmente são GUIDs.</span><span class="sxs-lookup"><span data-stu-id="131c7-125">Names for affinity groups created through the Management Portal are typically GUIDs.</span></span>
<span data-ttu-id="131c7-126">A porta de gerenciamento mostra o rótulo do grupo Affinity.</span><span class="sxs-lookup"><span data-stu-id="131c7-126">The Management Port shows the affinity group label.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131c7-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="131c7-127">-Profile</span></span>
<span data-ttu-id="131c7-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="131c7-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="131c7-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="131c7-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="131c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131c7-130">CommonParameters</span></span>
<span data-ttu-id="131c7-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="131c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131c7-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="131c7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131c7-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="131c7-133">INPUTS</span></span>

## <span data-ttu-id="131c7-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="131c7-134">OUTPUTS</span></span>

### <span data-ttu-id="131c7-135">AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="131c7-135">AffinityGroup</span></span>

## <span data-ttu-id="131c7-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="131c7-136">NOTES</span></span>

## <span data-ttu-id="131c7-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="131c7-137">RELATED LINKS</span></span>

[<span data-ttu-id="131c7-138">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="131c7-138">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="131c7-139">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="131c7-139">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="131c7-140">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="131c7-140">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


