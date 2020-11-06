---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 3e886803ff608522bd2d563dd9b6cd6effcfe074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440916"
---
# <span data-ttu-id="f166d-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f166d-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="f166d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f166d-102">SYNOPSIS</span></span>
<span data-ttu-id="f166d-103">Cria um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f166d-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f166d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f166d-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f166d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f166d-105">DESCRIPTION</span></span>
<span data-ttu-id="f166d-106">O cmdlet **New-AzureRmWebAppSlot** cria um slot do aplicativo Web do Azure em um determinado grupo de recursos que usa o plano do serviço de aplicativo especificado e o Data Center.</span><span class="sxs-lookup"><span data-stu-id="f166d-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="f166d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f166d-107">EXAMPLES</span></span>

### <span data-ttu-id="f166d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f166d-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="f166d-109">Esse comando cria um slot chamado Slot001 em um aplicativo Web existente nomes ContosoSite no grupo de recursos existente chamado padrão-Web-Oesteus no centro de dados oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="f166d-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="f166d-110">O comando usa um plano do serviço de aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f166d-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="f166d-111">OS</span><span class="sxs-lookup"><span data-stu-id="f166d-111">PARAMETERS</span></span>

### <span data-ttu-id="f166d-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f166d-112">-AppServicePlan</span></span>
<span data-ttu-id="f166d-113">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f166d-113">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="f166d-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="f166d-115">Configurações do aplicativo substitui Hashtable</span><span class="sxs-lookup"><span data-stu-id="f166d-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="f166d-116">-AseName</span></span>
<span data-ttu-id="f166d-117">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f166d-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f166d-118">-AseResourceGroupName</span></span>
<span data-ttu-id="f166d-119">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f166d-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-120">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="f166d-120">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="f166d-121">Opção ignorar nomes de host personalizados</span><span class="sxs-lookup"><span data-stu-id="f166d-121">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-122">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="f166d-122">-IgnoreSourceControl</span></span>
<span data-ttu-id="f166d-123">Opção ignorar controle de origem</span><span class="sxs-lookup"><span data-stu-id="f166d-123">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f166d-124">-Name</span></span>
<span data-ttu-id="f166d-125">Nome do webapp</span><span class="sxs-lookup"><span data-stu-id="f166d-125">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f166d-126">-ResourceGroupName</span></span>
<span data-ttu-id="f166d-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f166d-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="f166d-128">-Slot</span></span>
<span data-ttu-id="f166d-129">Nome do slot do webapp</span><span class="sxs-lookup"><span data-stu-id="f166d-129">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-130">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="f166d-130">-SourceWebApp</span></span>
<span data-ttu-id="f166d-131">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="f166d-131">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f166d-132">-DefaultProfile</span></span>
<span data-ttu-id="f166d-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f166d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f166d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f166d-134">CommonParameters</span></span>
<span data-ttu-id="f166d-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f166d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f166d-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f166d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f166d-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f166d-137">INPUTS</span></span>

### <span data-ttu-id="f166d-138">Instalação</span><span class="sxs-lookup"><span data-stu-id="f166d-138">Site</span></span>
<span data-ttu-id="f166d-139">O parâmetro ' SourceWebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="f166d-139">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f166d-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f166d-140">OUTPUTS</span></span>

## <span data-ttu-id="f166d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f166d-141">NOTES</span></span>

## <span data-ttu-id="f166d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f166d-142">RELATED LINKS</span></span>

[<span data-ttu-id="f166d-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f166d-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="f166d-144">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f166d-144">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="f166d-145">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f166d-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="f166d-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f166d-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="f166d-147">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f166d-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="f166d-148">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f166d-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="f166d-149">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f166d-149">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="f166d-150">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f166d-150">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
