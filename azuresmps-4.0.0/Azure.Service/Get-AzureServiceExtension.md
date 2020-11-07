---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2664607C-FF95-4EB7-869E-A421343B0517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 231f24a20471d8a4639b091c10d0e04f65b71b76
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945599"
---
# <span data-ttu-id="706d1-101">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="706d1-101">Get-AzureServiceExtension</span></span>

## <span data-ttu-id="706d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="706d1-102">SYNOPSIS</span></span>
<span data-ttu-id="706d1-103">Obtém extensões de serviço de nuvem que são aplicadas em uma implantação.</span><span class="sxs-lookup"><span data-stu-id="706d1-103">Gets cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="706d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="706d1-104">SYNTAX</span></span>

```
Get-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-ExtensionName] <String>]
 [[-ProviderNamespace] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="706d1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="706d1-105">DESCRIPTION</span></span>
<span data-ttu-id="706d1-106">O cmdlet **Get-AzureServiceExtension** Obtém extensões de serviço de nuvem existentes que são aplicadas em uma implantação.</span><span class="sxs-lookup"><span data-stu-id="706d1-106">The **Get-AzureServiceExtension** cmdlet gets existing cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="706d1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="706d1-107">EXAMPLES</span></span>

### <span data-ttu-id="706d1-108">Exemplo 1: obter uma extensão especificada</span><span class="sxs-lookup"><span data-stu-id="706d1-108">Example 1: Get a specified extension</span></span>
```
PS C:\> Get-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="706d1-109">Este comando obtém a extensão do serviço de nuvem com o nome e o namespace especificados.</span><span class="sxs-lookup"><span data-stu-id="706d1-109">This command gets the cloud service extension with the specified name and namespace.</span></span>

## <span data-ttu-id="706d1-110">OS</span><span class="sxs-lookup"><span data-stu-id="706d1-110">PARAMETERS</span></span>

### <span data-ttu-id="706d1-111">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="706d1-111">-ExtensionName</span></span>
<span data-ttu-id="706d1-112">Especifica o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="706d1-112">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="706d1-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="706d1-113">-InformationAction</span></span>
<span data-ttu-id="706d1-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="706d1-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="706d1-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="706d1-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="706d1-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="706d1-116">Continue</span></span>
- <span data-ttu-id="706d1-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="706d1-117">Ignore</span></span>
- <span data-ttu-id="706d1-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="706d1-118">Inquire</span></span>
- <span data-ttu-id="706d1-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="706d1-119">SilentlyContinue</span></span>
- <span data-ttu-id="706d1-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="706d1-120">Stop</span></span>
- <span data-ttu-id="706d1-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="706d1-121">Suspend</span></span>

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

### <span data-ttu-id="706d1-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="706d1-122">-InformationVariable</span></span>
<span data-ttu-id="706d1-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="706d1-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="706d1-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="706d1-124">-Profile</span></span>
<span data-ttu-id="706d1-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="706d1-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="706d1-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="706d1-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="706d1-127">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="706d1-127">-ProviderNamespace</span></span>
<span data-ttu-id="706d1-128">Especifica o namespace do provedor de extensão.</span><span class="sxs-lookup"><span data-stu-id="706d1-128">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="706d1-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="706d1-129">-ServiceName</span></span>
<span data-ttu-id="706d1-130">Especifica o nome do serviço do Azure da implantação.</span><span class="sxs-lookup"><span data-stu-id="706d1-130">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="706d1-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="706d1-131">-Slot</span></span>
<span data-ttu-id="706d1-132">Especifica o ambiente de implantação.</span><span class="sxs-lookup"><span data-stu-id="706d1-132">Specifies the deployment environment.</span></span>
<span data-ttu-id="706d1-133">Os valores aceitáveis para esse parâmetro são: produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="706d1-133">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="706d1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706d1-134">CommonParameters</span></span>
<span data-ttu-id="706d1-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="706d1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706d1-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="706d1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706d1-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="706d1-137">INPUTS</span></span>

## <span data-ttu-id="706d1-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="706d1-138">OUTPUTS</span></span>

## <span data-ttu-id="706d1-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="706d1-139">NOTES</span></span>

## <span data-ttu-id="706d1-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="706d1-140">RELATED LINKS</span></span>

[<span data-ttu-id="706d1-141">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="706d1-141">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)

[<span data-ttu-id="706d1-142">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="706d1-142">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


