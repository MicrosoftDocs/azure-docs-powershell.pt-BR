---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D08CB0A0-A0A9-4E0A-B1AB-A19A655B501B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5fd66813dcfc08f5e2f5276c4019443f9166945d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945596"
---
# <span data-ttu-id="45d87-101">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="45d87-101">Get-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="45d87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45d87-102">SYNOPSIS</span></span>
<span data-ttu-id="45d87-103">Esse cmdlet obtém a extensão da área de trabalho remota do serviço de nuvem aplicada a todas as funções ou funções nomeadas em um determinado slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="45d87-103">This cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="45d87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45d87-104">SYNTAX</span></span>

```
Get-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="45d87-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45d87-105">DESCRIPTION</span></span>
<span data-ttu-id="45d87-106">O cmdlet **Get-AzureServiceRemoteDesktopExtension** Obtém a extensão da área de trabalho remota do serviço de nuvem aplicada a todas as funções ou funções nomeadas em um determinado slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="45d87-106">The **Get-AzureServiceRemoteDesktopExtension** cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="45d87-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45d87-107">EXAMPLES</span></span>

### <span data-ttu-id="45d87-108">Exemplo 1: obter a extensão da área de trabalho remota para o serviço especificado</span><span class="sxs-lookup"><span data-stu-id="45d87-108">Example 1: Get remote desktop extension for the specified service</span></span>
```
PS C:\> Get-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="45d87-109">Este comando obtém a extensão da área de trabalho remota para o serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="45d87-109">This command gets the remote desktop extension for the specified service.</span></span>

## <span data-ttu-id="45d87-110">OS</span><span class="sxs-lookup"><span data-stu-id="45d87-110">PARAMETERS</span></span>

### <span data-ttu-id="45d87-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="45d87-111">-InformationAction</span></span>
<span data-ttu-id="45d87-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="45d87-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="45d87-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="45d87-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45d87-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="45d87-114">Continue</span></span>
- <span data-ttu-id="45d87-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="45d87-115">Ignore</span></span>
- <span data-ttu-id="45d87-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="45d87-116">Inquire</span></span>
- <span data-ttu-id="45d87-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="45d87-117">SilentlyContinue</span></span>
- <span data-ttu-id="45d87-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="45d87-118">Stop</span></span>
- <span data-ttu-id="45d87-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="45d87-119">Suspend</span></span>

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

### <span data-ttu-id="45d87-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="45d87-120">-InformationVariable</span></span>
<span data-ttu-id="45d87-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="45d87-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="45d87-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="45d87-122">-Profile</span></span>
<span data-ttu-id="45d87-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="45d87-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="45d87-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="45d87-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="45d87-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="45d87-125">-ServiceName</span></span>
<span data-ttu-id="45d87-126">Especifica o nome do serviço do Azure da implantação.</span><span class="sxs-lookup"><span data-stu-id="45d87-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="45d87-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="45d87-127">-Slot</span></span>
<span data-ttu-id="45d87-128">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="45d87-128">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="45d87-129">Os valores aceitáveis para esse parâmetro são: produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="45d87-129">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="45d87-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d87-130">CommonParameters</span></span>
<span data-ttu-id="45d87-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d87-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d87-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d87-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d87-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45d87-133">INPUTS</span></span>

## <span data-ttu-id="45d87-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45d87-134">OUTPUTS</span></span>

## <span data-ttu-id="45d87-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45d87-135">NOTES</span></span>

## <span data-ttu-id="45d87-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45d87-136">RELATED LINKS</span></span>

[<span data-ttu-id="45d87-137">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="45d87-137">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


