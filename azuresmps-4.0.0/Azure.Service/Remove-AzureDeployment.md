---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946165"
---
# <span data-ttu-id="ff23c-101">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff23c-101">Remove-AzureDeployment</span></span>

## <span data-ttu-id="ff23c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff23c-102">SYNOPSIS</span></span>
<span data-ttu-id="ff23c-103">Exclui uma implantação de um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="ff23c-103">Deletes a deployment of a cloud service.</span></span>

## <span data-ttu-id="ff23c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff23c-104">SYNTAX</span></span>

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff23c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff23c-105">DESCRIPTION</span></span>
<span data-ttu-id="ff23c-106">O cmdlet **Remove-AzureDeployment** exclui uma implantação de um serviço de nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff23c-106">The **Remove-AzureDeployment** cmdlet deletes a deployment of an Azure cloud service.</span></span>
<span data-ttu-id="ff23c-107">Para excluir uma implantação, primeiro suspenda-a.</span><span class="sxs-lookup"><span data-stu-id="ff23c-107">To delete a deployment, first suspend it.</span></span>

## <span data-ttu-id="ff23c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff23c-108">EXAMPLES</span></span>

### <span data-ttu-id="ff23c-109">Exemplo 1: remover uma implantação</span><span class="sxs-lookup"><span data-stu-id="ff23c-109">Example 1: Remove a deployment</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="ff23c-110">Esse comando Remove a implantação do serviço do Azure chamado ContosoService.</span><span class="sxs-lookup"><span data-stu-id="ff23c-110">This command removes the deployment of the Azure service named ContosoService.</span></span>
<span data-ttu-id="ff23c-111">Como esse comando não especifica um slot, ele remove o serviço do ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="ff23c-111">Because this command does not specify a slot, it removes the service from the production environment.</span></span>

### <span data-ttu-id="ff23c-112">Exemplo 2: remover uma implantação e discos rígidos virtuais</span><span class="sxs-lookup"><span data-stu-id="ff23c-112">Example 2: Remove a deployment and virtual hard disks</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

<span data-ttu-id="ff23c-113">Esse comando Remove a implantação do serviço denominado ContosoService do ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="ff23c-113">This command removes the deployment of the service named ContosoService from the production environment.</span></span>
<span data-ttu-id="ff23c-114">O comando também remove os discos rígidos virtuais subjacentes.</span><span class="sxs-lookup"><span data-stu-id="ff23c-114">The command also removes the underlying virtual hard disks.</span></span>

## <span data-ttu-id="ff23c-115">OS</span><span class="sxs-lookup"><span data-stu-id="ff23c-115">PARAMETERS</span></span>

### <span data-ttu-id="ff23c-116">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="ff23c-116">-DeleteVHD</span></span>
<span data-ttu-id="ff23c-117">Especifica que esse cmdlet Remove a implantação e os discos rígidos virtuais (VHDs) do armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="ff23c-117">Specifies that this cmdlet removes the deployment and the virtual hard disks (VHDs) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff23c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ff23c-118">-Force</span></span>
<span data-ttu-id="ff23c-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ff23c-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff23c-120">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ff23c-120">-InformationAction</span></span>
<span data-ttu-id="ff23c-121">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="ff23c-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff23c-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ff23c-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff23c-123">Contínuo</span><span class="sxs-lookup"><span data-stu-id="ff23c-123">Continue</span></span>
- <span data-ttu-id="ff23c-124">Ignorar</span><span class="sxs-lookup"><span data-stu-id="ff23c-124">Ignore</span></span>
- <span data-ttu-id="ff23c-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="ff23c-125">Inquire</span></span>
- <span data-ttu-id="ff23c-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff23c-126">SilentlyContinue</span></span>
- <span data-ttu-id="ff23c-127">Finaliza</span><span class="sxs-lookup"><span data-stu-id="ff23c-127">Stop</span></span>
- <span data-ttu-id="ff23c-128">Suspensão</span><span class="sxs-lookup"><span data-stu-id="ff23c-128">Suspend</span></span>

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

### <span data-ttu-id="ff23c-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff23c-129">-InformationVariable</span></span>
<span data-ttu-id="ff23c-130">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="ff23c-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff23c-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ff23c-131">-Profile</span></span>
<span data-ttu-id="ff23c-132">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ff23c-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff23c-133">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ff23c-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff23c-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ff23c-134">-ServiceName</span></span>
<span data-ttu-id="ff23c-135">Especifica o nome do serviço para o qual esse cmdlet exclui uma implantação.</span><span class="sxs-lookup"><span data-stu-id="ff23c-135">Specifies the name of the service for which this cmdlet deletes a deployment.</span></span>

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

### <span data-ttu-id="ff23c-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="ff23c-136">-Slot</span></span>
<span data-ttu-id="ff23c-137">Especifica o ambiente de implantação do qual esse cmdlet exclui a implantação.</span><span class="sxs-lookup"><span data-stu-id="ff23c-137">Specifies the deployment environment from which this cmdlet deletes the deployment.</span></span>
<span data-ttu-id="ff23c-138">Os valores válidos são: preparação e produção.</span><span class="sxs-lookup"><span data-stu-id="ff23c-138">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="ff23c-139">O valor padrão é produção.</span><span class="sxs-lookup"><span data-stu-id="ff23c-139">The default value is Production.</span></span>

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

### <span data-ttu-id="ff23c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff23c-140">CommonParameters</span></span>
<span data-ttu-id="ff23c-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff23c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff23c-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff23c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff23c-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff23c-143">INPUTS</span></span>

## <span data-ttu-id="ff23c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff23c-144">OUTPUTS</span></span>

### <span data-ttu-id="ff23c-145">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="ff23c-145">ManagementOperationContext</span></span>

## <span data-ttu-id="ff23c-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff23c-146">NOTES</span></span>

## <span data-ttu-id="ff23c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff23c-147">RELATED LINKS</span></span>

[<span data-ttu-id="ff23c-148">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff23c-148">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="ff23c-149">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="ff23c-149">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="ff23c-150">Mover-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff23c-150">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="ff23c-151">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff23c-151">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="ff23c-152">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff23c-152">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


