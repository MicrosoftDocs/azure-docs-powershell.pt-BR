---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 29602F63-A05B-45AF-8DD8-5EBBF4C33FCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32af8d2e89c14b0d36265efc688a88858851bba5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946172"
---
# <span data-ttu-id="afa16-101">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="afa16-101">Remove-AzureAffinityGroup</span></span>

## <span data-ttu-id="afa16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afa16-102">SYNOPSIS</span></span>
<span data-ttu-id="afa16-103">Exclui um grupo de afinidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="afa16-103">Deletes an affinity group in a subscription.</span></span>

## <span data-ttu-id="afa16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afa16-104">SYNTAX</span></span>

```
Remove-AzureAffinityGroup [-Name] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="afa16-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afa16-105">DESCRIPTION</span></span>
<span data-ttu-id="afa16-106">O cmdlet **Remove-AzureAffinityGroup** exclui um grupo de afinidade do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="afa16-106">The **Remove-AzureAffinityGroup** cmdlet deletes an Azure affinity group in the current subscription.</span></span>
<span data-ttu-id="afa16-107">Você não pode excluir um grupo de afinidade que tenha membros.</span><span class="sxs-lookup"><span data-stu-id="afa16-107">You cannot delete an affinity group that has any members.</span></span>
<span data-ttu-id="afa16-108">Você deve primeiro excluir todos os membros de um grupo de afinidade.</span><span class="sxs-lookup"><span data-stu-id="afa16-108">You must first delete all the members of an affinity group.</span></span>

## <span data-ttu-id="afa16-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afa16-109">EXAMPLES</span></span>

### <span data-ttu-id="afa16-110">Exemplo 1: remover um grupo de afinidade</span><span class="sxs-lookup"><span data-stu-id="afa16-110">Example 1: Remove an affinity group</span></span>
```
PS C:\> Remove-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="afa16-111">Esse comando exclui o grupo de afinidade South01 na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="afa16-111">This command deletes the South01 affinity group in the current subscription.</span></span>

## <span data-ttu-id="afa16-112">OS</span><span class="sxs-lookup"><span data-stu-id="afa16-112">PARAMETERS</span></span>

### <span data-ttu-id="afa16-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="afa16-113">-InformationAction</span></span>
<span data-ttu-id="afa16-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="afa16-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="afa16-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="afa16-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="afa16-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="afa16-116">Continue</span></span>
- <span data-ttu-id="afa16-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="afa16-117">Ignore</span></span>
- <span data-ttu-id="afa16-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="afa16-118">Inquire</span></span>
- <span data-ttu-id="afa16-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="afa16-119">SilentlyContinue</span></span>
- <span data-ttu-id="afa16-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="afa16-120">Stop</span></span>
- <span data-ttu-id="afa16-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="afa16-121">Suspend</span></span>

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

### <span data-ttu-id="afa16-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="afa16-122">-InformationVariable</span></span>
<span data-ttu-id="afa16-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="afa16-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="afa16-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="afa16-124">-Name</span></span>
<span data-ttu-id="afa16-125">Especifica o nome do grupo de afinidade que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="afa16-125">Specifies the name of the affinity group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="afa16-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="afa16-126">-Profile</span></span>
<span data-ttu-id="afa16-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="afa16-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="afa16-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="afa16-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="afa16-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa16-129">CommonParameters</span></span>
<span data-ttu-id="afa16-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa16-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa16-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa16-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa16-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afa16-132">INPUTS</span></span>

## <span data-ttu-id="afa16-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afa16-133">OUTPUTS</span></span>

## <span data-ttu-id="afa16-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afa16-134">NOTES</span></span>

## <span data-ttu-id="afa16-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afa16-135">RELATED LINKS</span></span>

[<span data-ttu-id="afa16-136">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="afa16-136">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="afa16-137">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="afa16-137">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="afa16-138">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="afa16-138">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


