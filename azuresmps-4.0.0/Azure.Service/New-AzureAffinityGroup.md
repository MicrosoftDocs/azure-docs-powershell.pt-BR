---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946227"
---
# <span data-ttu-id="bfb5c-101">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="bfb5c-101">New-AzureAffinityGroup</span></span>

## <span data-ttu-id="bfb5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfb5c-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb5c-103">Cria um grupo de afinidade na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-103">Creates an affinity group in the current subscription.</span></span>

## <span data-ttu-id="bfb5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfb5c-104">SYNTAX</span></span>

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfb5c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfb5c-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb5c-106">O cmdlet **New-AzureAffinityGroup** cria um grupo de afinidade do Azure na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-106">The **New-AzureAffinityGroup** cmdlet creates an Azure affinity group in the current Azure subscription.</span></span>

<span data-ttu-id="bfb5c-107">Um grupo de afinidade coloca seus serviços e seus recursos juntos em um datacenter do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-107">An affinity group puts your services and their resources together in an Azure datacenter.</span></span>
<span data-ttu-id="bfb5c-108">O grupo de afinidade agrupa os membros em conjunto para o desempenho ideal.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-108">The affinity group groups members together for optimal performance.</span></span>
<span data-ttu-id="bfb5c-109">Defina grupos de afinidade no nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-109">Define affinity groups at the subscription level.</span></span>
<span data-ttu-id="bfb5c-110">Seus grupos de afinidade estão disponíveis para todos os serviços de nuvem ou contas de armazenamento subsequentes que você criar.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-110">Your affinity groups are available to any subsequent cloud services or storage accounts that you create.</span></span>
<span data-ttu-id="bfb5c-111">Você pode adicionar serviços a um grupo de afinidade somente quando criá-lo.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-111">You can add services to an affinity group only when you create it.</span></span>

## <span data-ttu-id="bfb5c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfb5c-112">EXAMPLES</span></span>

### <span data-ttu-id="bfb5c-113">Exemplo 1: criar um grupo de afinidade</span><span class="sxs-lookup"><span data-stu-id="bfb5c-113">Example 1: Create an affinity group</span></span>
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

<span data-ttu-id="bfb5c-114">Esse comando cria um grupo de afinidade chamado South01 na região centro dos EUA do Sul.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-114">This command creates an affinity group named South01 in the South Central US region.</span></span>
<span data-ttu-id="bfb5c-115">O comando especifica um rótulo e uma descrição.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-115">The command specifies a label and a description.</span></span>

## <span data-ttu-id="bfb5c-116">OS</span><span class="sxs-lookup"><span data-stu-id="bfb5c-116">PARAMETERS</span></span>

### <span data-ttu-id="bfb5c-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="bfb5c-117">-Description</span></span>
<span data-ttu-id="bfb5c-118">Especifica uma descrição para o grupo de afinidade.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-118">Specifies a description for the affinity group.</span></span>
<span data-ttu-id="bfb5c-119">A descrição pode ter até 1024 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-119">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="bfb5c-120">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bfb5c-120">-InformationAction</span></span>
<span data-ttu-id="bfb5c-121">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bfb5c-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bfb5c-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bfb5c-123">Contínuo</span><span class="sxs-lookup"><span data-stu-id="bfb5c-123">Continue</span></span>
- <span data-ttu-id="bfb5c-124">Ignorar</span><span class="sxs-lookup"><span data-stu-id="bfb5c-124">Ignore</span></span>
- <span data-ttu-id="bfb5c-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="bfb5c-125">Inquire</span></span>
- <span data-ttu-id="bfb5c-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bfb5c-126">SilentlyContinue</span></span>
- <span data-ttu-id="bfb5c-127">Finaliza</span><span class="sxs-lookup"><span data-stu-id="bfb5c-127">Stop</span></span>
- <span data-ttu-id="bfb5c-128">Suspensão</span><span class="sxs-lookup"><span data-stu-id="bfb5c-128">Suspend</span></span>

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

### <span data-ttu-id="bfb5c-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bfb5c-129">-InformationVariable</span></span>
<span data-ttu-id="bfb5c-130">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bfb5c-131">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="bfb5c-131">-Label</span></span>
<span data-ttu-id="bfb5c-132">Especifica um rótulo para o grupo de afinidade.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-132">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="bfb5c-133">O rótulo pode ter até 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-133">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="bfb5c-134">-Local</span><span class="sxs-lookup"><span data-stu-id="bfb5c-134">-Location</span></span>
<span data-ttu-id="bfb5c-135">Especifica a localização geográfica do Azure datacenter em que esse cmdlet cria o grupo de afinidade.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-135">Specifies the geographical location of the Azure datacenter where this cmdlet creates the affinity group.</span></span>

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

### <span data-ttu-id="bfb5c-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfb5c-136">-Name</span></span>
<span data-ttu-id="bfb5c-137">Especifica um nome para o grupo de afinidade.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-137">Specifies a name for the affinity group.</span></span>
<span data-ttu-id="bfb5c-138">O nome deve ser exclusivo para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-138">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="bfb5c-139">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bfb5c-139">-Profile</span></span>
<span data-ttu-id="bfb5c-140">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bfb5c-141">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bfb5c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb5c-142">CommonParameters</span></span>
<span data-ttu-id="bfb5c-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb5c-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb5c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb5c-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfb5c-145">INPUTS</span></span>

## <span data-ttu-id="bfb5c-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfb5c-146">OUTPUTS</span></span>

## <span data-ttu-id="bfb5c-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfb5c-147">NOTES</span></span>

## <span data-ttu-id="bfb5c-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfb5c-148">RELATED LINKS</span></span>

[<span data-ttu-id="bfb5c-149">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="bfb5c-149">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="bfb5c-150">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="bfb5c-150">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="bfb5c-151">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="bfb5c-151">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


