---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946431"
---
# <span data-ttu-id="e36c7-101">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e36c7-101">Set-AzureAffinityGroup</span></span>

## <span data-ttu-id="e36c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e36c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e36c7-103">Modifica as propriedades de um grupo de afinidade.</span><span class="sxs-lookup"><span data-stu-id="e36c7-103">Modifies properties of an affinity group.</span></span>

## <span data-ttu-id="e36c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e36c7-104">SYNTAX</span></span>

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e36c7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e36c7-105">DESCRIPTION</span></span>
<span data-ttu-id="e36c7-106">O cmdlet **set-AzureAffinityGroup** modifica as propriedades de um grupo de afinidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="e36c7-106">The **Set-AzureAffinityGroup** cmdlet modifies properties of an Azure affinity group.</span></span>
<span data-ttu-id="e36c7-107">Você pode alterar o rótulo e a descrição.</span><span class="sxs-lookup"><span data-stu-id="e36c7-107">You can change the label and the description.</span></span>

## <span data-ttu-id="e36c7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e36c7-108">EXAMPLES</span></span>

### <span data-ttu-id="e36c7-109">Exemplo 1: modificar um grupo de afinidade</span><span class="sxs-lookup"><span data-stu-id="e36c7-109">Example 1: Modify an affinity group</span></span>
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

<span data-ttu-id="e36c7-110">Esse comando modifica o rótulo do grupo de afinidade chamado South01 para ser SouthUSProduction o comando também modifica a descrição.</span><span class="sxs-lookup"><span data-stu-id="e36c7-110">This command modifies the label of the affinity group named South01 to be SouthUSProduction The command also modifies the description.</span></span>

## <span data-ttu-id="e36c7-111">OS</span><span class="sxs-lookup"><span data-stu-id="e36c7-111">PARAMETERS</span></span>

### <span data-ttu-id="e36c7-112">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e36c7-112">-Description</span></span>
<span data-ttu-id="e36c7-113">Especifica a descrição do grupo de afinidade.</span><span class="sxs-lookup"><span data-stu-id="e36c7-113">Specifies the description of the affinity group.</span></span>
<span data-ttu-id="e36c7-114">A descrição pode ter até 1024 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="e36c7-114">The description can be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36c7-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e36c7-115">-InformationAction</span></span>
<span data-ttu-id="e36c7-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="e36c7-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e36c7-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e36c7-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e36c7-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="e36c7-118">Continue</span></span>
- <span data-ttu-id="e36c7-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e36c7-119">Ignore</span></span>
- <span data-ttu-id="e36c7-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="e36c7-120">Inquire</span></span>
- <span data-ttu-id="e36c7-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e36c7-121">SilentlyContinue</span></span>
- <span data-ttu-id="e36c7-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="e36c7-122">Stop</span></span>
- <span data-ttu-id="e36c7-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="e36c7-123">Suspend</span></span>

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

### <span data-ttu-id="e36c7-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e36c7-124">-InformationVariable</span></span>
<span data-ttu-id="e36c7-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="e36c7-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e36c7-126">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="e36c7-126">-Label</span></span>
<span data-ttu-id="e36c7-127">Especifica um rótulo para o grupo de afinidade.</span><span class="sxs-lookup"><span data-stu-id="e36c7-127">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="e36c7-128">O rótulo pode ter até 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="e36c7-128">The label can be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36c7-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e36c7-129">-Name</span></span>
<span data-ttu-id="e36c7-130">Especifica o nome do grupo de afinidade que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e36c7-130">Specifies the name of the affinity group that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36c7-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e36c7-131">-Profile</span></span>
<span data-ttu-id="e36c7-132">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e36c7-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e36c7-133">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e36c7-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e36c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36c7-134">CommonParameters</span></span>
<span data-ttu-id="e36c7-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36c7-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36c7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36c7-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e36c7-137">INPUTS</span></span>

## <span data-ttu-id="e36c7-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e36c7-138">OUTPUTS</span></span>

## <span data-ttu-id="e36c7-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e36c7-139">NOTES</span></span>

## <span data-ttu-id="e36c7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e36c7-140">RELATED LINKS</span></span>

[<span data-ttu-id="e36c7-141">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e36c7-141">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="e36c7-142">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e36c7-142">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="e36c7-143">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e36c7-143">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)


