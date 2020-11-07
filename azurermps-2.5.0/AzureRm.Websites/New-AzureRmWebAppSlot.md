---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: f41149c6abb946340acc06b847c72dcabcee18fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785588"
---
# <span data-ttu-id="45c4d-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45c4d-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="45c4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="45c4d-103">Cria um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="45c4d-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45c4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45c4d-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45c4d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="45c4d-106">O cmdlet **New-AzureRmWebAppSlot** cria um slot do aplicativo Web do Azure em um determinado grupo de recursos que usa o plano do serviço de aplicativo especificado e o Data Center.</span><span class="sxs-lookup"><span data-stu-id="45c4d-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="45c4d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45c4d-107">EXAMPLES</span></span>

### <span data-ttu-id="45c4d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45c4d-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="45c4d-109">Esse comando cria um slot chamado Slot001 em um aplicativo Web existente nomes ContosoSite no grupo de recursos existente chamado padrão-Web-Oesteus no centro de dados oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="45c4d-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="45c4d-110">O comando usa um plano do serviço de aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="45c4d-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="45c4d-111">OS</span><span class="sxs-lookup"><span data-stu-id="45c4d-111">PARAMETERS</span></span>

### <span data-ttu-id="45c4d-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="45c4d-112">-AppServicePlan</span></span>
<span data-ttu-id="45c4d-113">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="45c4d-113">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="45c4d-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="45c4d-115">Configurações do aplicativo substitui Hashtable</span><span class="sxs-lookup"><span data-stu-id="45c4d-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="45c4d-116">-AseName</span></span>
<span data-ttu-id="45c4d-117">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="45c4d-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c4d-118">-AseResourceGroupName</span></span>
<span data-ttu-id="45c4d-119">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="45c4d-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c4d-120">-DefaultProfile</span></span>
<span data-ttu-id="45c4d-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45c4d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="45c4d-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="45c4d-123">Opção ignorar nomes de host personalizados</span><span class="sxs-lookup"><span data-stu-id="45c4d-123">Ignore Custom HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="45c4d-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="45c4d-125">Opção ignorar controle de origem</span><span class="sxs-lookup"><span data-stu-id="45c4d-125">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="45c4d-126">-Name</span></span>
<span data-ttu-id="45c4d-127">Nome do webapp</span><span class="sxs-lookup"><span data-stu-id="45c4d-127">Webapp Name</span></span>

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

### <span data-ttu-id="45c4d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c4d-128">-ResourceGroupName</span></span>
<span data-ttu-id="45c4d-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="45c4d-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="45c4d-130">-Slot</span></span>
<span data-ttu-id="45c4d-131">Nome do slot do webapp</span><span class="sxs-lookup"><span data-stu-id="45c4d-131">Webapp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="45c4d-132">-SourceWebApp</span></span>
<span data-ttu-id="45c4d-133">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="45c4d-133">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45c4d-134">-AsJob</span></span>
<span data-ttu-id="45c4d-135">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="45c4d-135">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c4d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c4d-136">CommonParameters</span></span>
<span data-ttu-id="45c4d-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c4d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c4d-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45c4d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c4d-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45c4d-139">INPUTS</span></span>

### <span data-ttu-id="45c4d-140">Instalação</span><span class="sxs-lookup"><span data-stu-id="45c4d-140">Site</span></span>
<span data-ttu-id="45c4d-141">O parâmetro ' SourceWebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="45c4d-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="45c4d-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45c4d-142">OUTPUTS</span></span>

## <span data-ttu-id="45c4d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45c4d-143">NOTES</span></span>

## <span data-ttu-id="45c4d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45c4d-144">RELATED LINKS</span></span>

[<span data-ttu-id="45c4d-145">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45c4d-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="45c4d-146">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45c4d-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="45c4d-147">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45c4d-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="45c4d-148">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45c4d-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="45c4d-149">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45c4d-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="45c4d-150">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45c4d-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="45c4d-151">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="45c4d-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="45c4d-152">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="45c4d-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
