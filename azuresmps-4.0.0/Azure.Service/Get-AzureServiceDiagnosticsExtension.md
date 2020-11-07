---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 235DD5D7-BE24-4FBE-88E2-40D1943ED155
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4fb3f35bc64a1431550d4da5aa669e934cd3a7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945603"
---
# <span data-ttu-id="cb609-101">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cb609-101">Get-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="cb609-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb609-102">SYNOPSIS</span></span>
<span data-ttu-id="cb609-103">Obtém a extensão do diagnóstico do serviço de nuvem aplicada a todas as funções ou funções nomeadas em um determinado slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="cb609-103">Gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="cb609-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb609-104">SYNTAX</span></span>

```
Get-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb609-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb609-105">DESCRIPTION</span></span>
<span data-ttu-id="cb609-106">O cmdlet **Get-AzureServiceDiagnosticsExtension** Obtém a extensão do diagnóstico do serviço em nuvem aplicada a todas as funções ou funções nomeadas em um determinado slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="cb609-106">The **Get-AzureServiceDiagnosticsExtension** cmdlet gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="cb609-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb609-107">EXAMPLES</span></span>

### <span data-ttu-id="cb609-108">Exemplo 1: obter extensão de diagnóstico do serviço</span><span class="sxs-lookup"><span data-stu-id="cb609-108">Example 1: Get service diagnostics extension</span></span> 
```
PS C:\> Get-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="cb609-109">Esse comando obtém o diagnóstico do serviço para um serviço, em todas as funções.</span><span class="sxs-lookup"><span data-stu-id="cb609-109">This command gets the service diagnostics for a service, across all roles.</span></span>

## <span data-ttu-id="cb609-110">OS</span><span class="sxs-lookup"><span data-stu-id="cb609-110">PARAMETERS</span></span>

### <span data-ttu-id="cb609-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cb609-111">-InformationAction</span></span>
<span data-ttu-id="cb609-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="cb609-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cb609-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cb609-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb609-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="cb609-114">Continue</span></span>
- <span data-ttu-id="cb609-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="cb609-115">Ignore</span></span>
- <span data-ttu-id="cb609-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="cb609-116">Inquire</span></span>
- <span data-ttu-id="cb609-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cb609-117">SilentlyContinue</span></span>
- <span data-ttu-id="cb609-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="cb609-118">Stop</span></span>
- <span data-ttu-id="cb609-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="cb609-119">Suspend</span></span>

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

### <span data-ttu-id="cb609-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cb609-120">-InformationVariable</span></span>
<span data-ttu-id="cb609-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="cb609-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cb609-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="cb609-122">-Profile</span></span>
<span data-ttu-id="cb609-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="cb609-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cb609-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="cb609-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cb609-125">-Função</span><span class="sxs-lookup"><span data-stu-id="cb609-125">-Role</span></span>
<span data-ttu-id="cb609-126">Especifica uma matriz de funções.</span><span class="sxs-lookup"><span data-stu-id="cb609-126">Specifies an array of roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb609-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cb609-127">-ServiceName</span></span>
<span data-ttu-id="cb609-128">Especifica o nome do serviço do Azure da implantação.</span><span class="sxs-lookup"><span data-stu-id="cb609-128">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="cb609-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="cb609-129">-Slot</span></span>
<span data-ttu-id="cb609-130">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="cb609-130">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="cb609-131">Os valores aceitáveis para esse parâmetro são: produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="cb609-131">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="cb609-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb609-132">CommonParameters</span></span>
<span data-ttu-id="cb609-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb609-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb609-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb609-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb609-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb609-135">INPUTS</span></span>

## <span data-ttu-id="cb609-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb609-136">OUTPUTS</span></span>

## <span data-ttu-id="cb609-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb609-137">NOTES</span></span>

## <span data-ttu-id="cb609-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb609-138">RELATED LINKS</span></span>

[<span data-ttu-id="cb609-139">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cb609-139">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="cb609-140">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cb609-140">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


