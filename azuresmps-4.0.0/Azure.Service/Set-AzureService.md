---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A920D84-0005-45A2-8229-FD9436A2CA6D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 927520466299776326229976b355444f9db6c23e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946049"
---
# <span data-ttu-id="627fb-101">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="627fb-101">Set-AzureService</span></span>

## <span data-ttu-id="627fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="627fb-102">SYNOPSIS</span></span>
<span data-ttu-id="627fb-103">Define ou atualiza o rótulo e a descrição do serviço do Microsoft Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="627fb-103">Sets or updates the label and description of the specified Microsoft Azure service.</span></span>

## <span data-ttu-id="627fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="627fb-104">SYNTAX</span></span>

```
Set-AzureService [-ServiceName] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="627fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="627fb-105">DESCRIPTION</span></span>
<span data-ttu-id="627fb-106">O cmdlet **set-AzureService** atribui um rótulo e uma descrição a um serviço na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="627fb-106">The **Set-AzureService** cmdlet assigns a label and description to a service in the current subscription.</span></span>

## <span data-ttu-id="627fb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="627fb-107">EXAMPLES</span></span>

### <span data-ttu-id="627fb-108">Exemplo 1: atualizar o rótulo e a descrição de um serviço</span><span class="sxs-lookup"><span data-stu-id="627fb-108">Example 1: Update the label and description for a service</span></span>
```
PS C:\> C:\PS>Set-AzureService -ServiceName "MySvc1" -Label "MyTestSvc1" -Description "My service for testing out new configurations"
```

<span data-ttu-id="627fb-109">Esse comando define o rótulo como "MyTestSvc1" e a descrição para "meu serviço para testar novas configurações" para o serviço MyTestSvc1.</span><span class="sxs-lookup"><span data-stu-id="627fb-109">This command sets the label to "MyTestSvc1" and the description to "My service for testing out new configurations" for the MyTestSvc1 service.</span></span>

## <span data-ttu-id="627fb-110">OS</span><span class="sxs-lookup"><span data-stu-id="627fb-110">PARAMETERS</span></span>

### <span data-ttu-id="627fb-111">-Descrição</span><span class="sxs-lookup"><span data-stu-id="627fb-111">-Description</span></span>
<span data-ttu-id="627fb-112">Especifica uma descrição para o serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="627fb-112">Specifies a description for the Azure service.</span></span>
<span data-ttu-id="627fb-113">A descrição pode ter até 1024 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="627fb-113">The description may be up to 1024 characters in length.</span></span>

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

### <span data-ttu-id="627fb-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="627fb-114">-InformationAction</span></span>
<span data-ttu-id="627fb-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="627fb-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="627fb-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="627fb-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="627fb-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="627fb-117">Continue</span></span>
- <span data-ttu-id="627fb-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="627fb-118">Ignore</span></span>
- <span data-ttu-id="627fb-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="627fb-119">Inquire</span></span>
- <span data-ttu-id="627fb-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="627fb-120">SilentlyContinue</span></span>
- <span data-ttu-id="627fb-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="627fb-121">Stop</span></span>
- <span data-ttu-id="627fb-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="627fb-122">Suspend</span></span>

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

### <span data-ttu-id="627fb-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="627fb-123">-InformationVariable</span></span>
<span data-ttu-id="627fb-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="627fb-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="627fb-125">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="627fb-125">-Label</span></span>
<span data-ttu-id="627fb-126">Especifica um rótulo para o serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="627fb-126">Specifies a label for the Azure service.</span></span>
<span data-ttu-id="627fb-127">O rótulo pode ter até 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="627fb-127">The label may be up to 100 characters in length.</span></span>

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

### <span data-ttu-id="627fb-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="627fb-128">-Profile</span></span>
<span data-ttu-id="627fb-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="627fb-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="627fb-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="627fb-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="627fb-131">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="627fb-131">-ReverseDnsFqdn</span></span>
<span data-ttu-id="627fb-132">Especifica o nome de domínio totalmente qualificado para DNS reverso.</span><span class="sxs-lookup"><span data-stu-id="627fb-132">Specifies the fully qualified domain name for reverse DNS.</span></span>

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

### <span data-ttu-id="627fb-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="627fb-133">-ServiceName</span></span>
<span data-ttu-id="627fb-134">Especifica o nome do serviço do Azure a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="627fb-134">Specifies the name of the Azure service to update.</span></span>

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

### <span data-ttu-id="627fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627fb-135">CommonParameters</span></span>
<span data-ttu-id="627fb-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="627fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627fb-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="627fb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627fb-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="627fb-138">INPUTS</span></span>

## <span data-ttu-id="627fb-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="627fb-139">OUTPUTS</span></span>

### <span data-ttu-id="627fb-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="627fb-140">ManagementOperationContext</span></span>

## <span data-ttu-id="627fb-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="627fb-141">NOTES</span></span>

## <span data-ttu-id="627fb-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="627fb-142">RELATED LINKS</span></span>

[<span data-ttu-id="627fb-143">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="627fb-143">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="627fb-144">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="627fb-144">New-AzureService</span></span>](./New-AzureService.md)


