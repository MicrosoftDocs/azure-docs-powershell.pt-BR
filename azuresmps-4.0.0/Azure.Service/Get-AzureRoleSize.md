---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2CBF8DEF-954C-4D9F-B495-C2F76550BC79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f7e8a7a08ac2793b7e4aeb8615e5fb8fc1f727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945615"
---
# <span data-ttu-id="5a853-101">Get-AzureRoleSize</span><span class="sxs-lookup"><span data-stu-id="5a853-101">Get-AzureRoleSize</span></span>

## <span data-ttu-id="5a853-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a853-102">SYNOPSIS</span></span>
<span data-ttu-id="5a853-103">Obtém as informações de tamanho da função para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="5a853-103">Gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="5a853-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a853-104">SYNTAX</span></span>

```
Get-AzureRoleSize [[-InstanceSize] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5a853-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a853-105">DESCRIPTION</span></span>
<span data-ttu-id="5a853-106">O cmdlet **Get-AzureRoleSize** Obtém as informações de tamanho da função para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="5a853-106">The **Get-AzureRoleSize** cmdlet gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="5a853-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a853-107">EXAMPLES</span></span>

### <span data-ttu-id="5a853-108">Exemplo 1: obter informações de tamanho da função</span><span class="sxs-lookup"><span data-stu-id="5a853-108">Example 1: Get role size information</span></span>
```
PS C:\> Get-AzureRoleSize

          InstanceSize               : A6
          RoleSizeLabel              :
          Cores                      : 4
          MemoryInMb                 : 28672
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="5a853-109">Este comando obtém informações de tamanho da função para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="5a853-109">This command gets role size information for the current subscription.</span></span>

### <span data-ttu-id="5a853-110">Exemplo 2: obter informações de tamanho da função e especificar o nome do tamanho da função</span><span class="sxs-lookup"><span data-stu-id="5a853-110">Example 2: Get role size information and specify the role size name</span></span>
```
PS C:\> Get-AzureRoleSize -InstanceSize A7

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="5a853-111">Este comando obtém informações de tamanho da função para o tamanho de função especificado.</span><span class="sxs-lookup"><span data-stu-id="5a853-111">This command gets role size information for the specified role size.</span></span>

### <span data-ttu-id="5a853-112">Exemplo 3: obter informações de tamanho de função para todas as máquinas virtuais em todos os serviços do Azure</span><span class="sxs-lookup"><span data-stu-id="5a853-112">Example 3: Get role size information for all virtual machines in all of the Azure services</span></span>
```
PS C:\> Get-AzureService | Get-AzureVM | Get-AzureRoleSize
```

<span data-ttu-id="5a853-113">Esse comando obtém informações de tamanho da função para todas as máquinas virtuais em todos os serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a853-113">This command gets role size information for all virtual machines in all of the Azure services.</span></span>

## <span data-ttu-id="5a853-114">OS</span><span class="sxs-lookup"><span data-stu-id="5a853-114">PARAMETERS</span></span>

### <span data-ttu-id="5a853-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="5a853-115">-InformationAction</span></span>
<span data-ttu-id="5a853-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="5a853-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5a853-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5a853-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a853-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="5a853-118">Continue</span></span>
- <span data-ttu-id="5a853-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="5a853-119">Ignore</span></span>
- <span data-ttu-id="5a853-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="5a853-120">Inquire</span></span>
- <span data-ttu-id="5a853-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5a853-121">SilentlyContinue</span></span>
- <span data-ttu-id="5a853-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="5a853-122">Stop</span></span>
- <span data-ttu-id="5a853-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="5a853-123">Suspend</span></span>

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

### <span data-ttu-id="5a853-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5a853-124">-InformationVariable</span></span>
<span data-ttu-id="5a853-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="5a853-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5a853-126">-Instanceize</span><span class="sxs-lookup"><span data-stu-id="5a853-126">-InstanceSize</span></span>
<span data-ttu-id="5a853-127">Especifica o nome do tamanho da função, por exemplo: ExtraSmall, pequeno, grande, ExtraLarge, a5, A6, A7.</span><span class="sxs-lookup"><span data-stu-id="5a853-127">Specifies the role size name, for example: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span></span>

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

### <span data-ttu-id="5a853-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5a853-128">-Profile</span></span>
<span data-ttu-id="5a853-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5a853-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a853-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5a853-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a853-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a853-131">CommonParameters</span></span>
<span data-ttu-id="5a853-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a853-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a853-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a853-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a853-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a853-134">INPUTS</span></span>

## <span data-ttu-id="5a853-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a853-135">OUTPUTS</span></span>

## <span data-ttu-id="5a853-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a853-136">NOTES</span></span>

## <span data-ttu-id="5a853-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a853-137">RELATED LINKS</span></span>

[<span data-ttu-id="5a853-138">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="5a853-138">Get-AzureRole</span></span>](./Get-AzureRole.md)

[<span data-ttu-id="5a853-139">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="5a853-139">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="5a853-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="5a853-140">Get-AzureVM</span></span>](./Get-AzureVM.md)


