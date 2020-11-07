---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F3BC5AF-8D7B-40BF-A072-A11C7BDCB6B3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09adc7e9b2faf9b9a905fa1c94fb6526e02c110f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945786"
---
# <span data-ttu-id="4f985-101">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="4f985-101">Set-AzureWalkUpgradeDomain</span></span>

## <span data-ttu-id="4f985-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f985-102">SYNOPSIS</span></span>
<span data-ttu-id="4f985-103">Orienta o domínio de atualização especificado.</span><span class="sxs-lookup"><span data-stu-id="4f985-103">Walks the specified upgrade domain.</span></span>

## <span data-ttu-id="4f985-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f985-104">SYNTAX</span></span>

```
Set-AzureWalkUpgradeDomain [-ServiceName] <String> [-Slot] <String> [-DomainNumber] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f985-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f985-105">DESCRIPTION</span></span>
<span data-ttu-id="4f985-106">O cmdlet **set-AzureWalkUpgradeDomain** inicia a atualização real de uma implantação do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f985-106">The **Set-AzureWalkUpgradeDomain** cmdlet initiates the actual upgrade of an Azure deployment.</span></span>
<span data-ttu-id="4f985-107">O pacote de atualização e a configuração são definidos usando o cmdlet **set-AzureDeployment** com a opção-upgrade.</span><span class="sxs-lookup"><span data-stu-id="4f985-107">The upgrade package and configuration are set by using the **Set-AzureDeployment** cmdlet with the -Upgrade switch.</span></span>

## <span data-ttu-id="4f985-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f985-108">EXAMPLES</span></span>

### <span data-ttu-id="4f985-109">Exemplo 1: iniciar uma atualização de uma implantação de produção</span><span class="sxs-lookup"><span data-stu-id="4f985-109">Example 1: Initiate an upgrade of a production deployment</span></span>
```
PS C:\> Set-AzureWalkUpgradeDomain -ServiceName "MySvc1" -slot "Production" -UpgradeDomain 2
```

<span data-ttu-id="4f985-110">Este comando inicia a atualização do domínio de atualização 2 da implantação de produção do serviço MySvc1.</span><span class="sxs-lookup"><span data-stu-id="4f985-110">This command initiates the upgrade of Upgrade Domain 2 of the production deployment of the MySvc1 service.</span></span>

## <span data-ttu-id="4f985-111">OS</span><span class="sxs-lookup"><span data-stu-id="4f985-111">PARAMETERS</span></span>

### <span data-ttu-id="4f985-112">-DomainNumber</span><span class="sxs-lookup"><span data-stu-id="4f985-112">-DomainNumber</span></span>
<span data-ttu-id="4f985-113">Especifica o domínio de atualização a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4f985-113">Specifies the upgrade domain to upgrade.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f985-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="4f985-114">-InformationAction</span></span>
<span data-ttu-id="4f985-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="4f985-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4f985-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4f985-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f985-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="4f985-117">Continue</span></span>
- <span data-ttu-id="4f985-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="4f985-118">Ignore</span></span>
- <span data-ttu-id="4f985-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="4f985-119">Inquire</span></span>
- <span data-ttu-id="4f985-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f985-120">SilentlyContinue</span></span>
- <span data-ttu-id="4f985-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="4f985-121">Stop</span></span>
- <span data-ttu-id="4f985-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="4f985-122">Suspend</span></span>

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

### <span data-ttu-id="4f985-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f985-123">-InformationVariable</span></span>
<span data-ttu-id="4f985-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="4f985-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4f985-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4f985-125">-Profile</span></span>
<span data-ttu-id="4f985-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4f985-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f985-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4f985-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f985-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4f985-128">-ServiceName</span></span>
<span data-ttu-id="4f985-129">Especifica o nome do serviço do Microsoft Azure a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4f985-129">Specifies the Microsoft Azure service name to upgrade.</span></span>

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

### <span data-ttu-id="4f985-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="4f985-130">-Slot</span></span>
<span data-ttu-id="4f985-131">Especifica o ambiente da implantação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="4f985-131">Specifies the environment of the deployment to upgrade.</span></span>

<span data-ttu-id="4f985-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4f985-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f985-133">Preparação</span><span class="sxs-lookup"><span data-stu-id="4f985-133">Staging</span></span>
- <span data-ttu-id="4f985-134">Preparo</span><span class="sxs-lookup"><span data-stu-id="4f985-134">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f985-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f985-135">CommonParameters</span></span>
<span data-ttu-id="4f985-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f985-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f985-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f985-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f985-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f985-138">INPUTS</span></span>

## <span data-ttu-id="4f985-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f985-139">OUTPUTS</span></span>

### <span data-ttu-id="4f985-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="4f985-140">ManagementOperationContext</span></span>

## <span data-ttu-id="4f985-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f985-141">NOTES</span></span>

## <span data-ttu-id="4f985-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f985-142">RELATED LINKS</span></span>

[<span data-ttu-id="4f985-143">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4f985-143">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


