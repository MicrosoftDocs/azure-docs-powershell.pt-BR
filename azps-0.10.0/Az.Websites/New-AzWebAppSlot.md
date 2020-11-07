---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 41851c1492c3c14e3129ba04367580b09cf3ffb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776082"
---
# <span data-ttu-id="f8392-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8392-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="f8392-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8392-102">SYNOPSIS</span></span>
<span data-ttu-id="f8392-103">Cria um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f8392-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="f8392-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8392-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8392-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8392-105">DESCRIPTION</span></span>
<span data-ttu-id="f8392-106">O cmdlet **New-AzWebAppSlot** cria um slot do aplicativo Web do Azure em um determinado grupo de recursos que usa o plano do serviço de aplicativo especificado e o Data Center.</span><span class="sxs-lookup"><span data-stu-id="f8392-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="f8392-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8392-107">EXAMPLES</span></span>

### <span data-ttu-id="f8392-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8392-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="f8392-109">Esse comando cria um slot chamado Slot001 em um aplicativo Web existente nomes ContosoSite no grupo de recursos existente chamado padrão-Web-Oesteus no centro de dados oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="f8392-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="f8392-110">O comando usa um plano do serviço de aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f8392-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="f8392-111">OS</span><span class="sxs-lookup"><span data-stu-id="f8392-111">PARAMETERS</span></span>

### <span data-ttu-id="f8392-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f8392-112">-AppServicePlan</span></span>
<span data-ttu-id="f8392-113">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f8392-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="f8392-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="f8392-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="f8392-115">Configurações do aplicativo substitui Hashtable</span><span class="sxs-lookup"><span data-stu-id="f8392-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="f8392-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="f8392-116">-AseName</span></span>
<span data-ttu-id="f8392-117">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f8392-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="f8392-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8392-118">-AseResourceGroupName</span></span>
<span data-ttu-id="f8392-119">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f8392-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="f8392-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8392-120">-DefaultProfile</span></span>
<span data-ttu-id="f8392-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8392-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8392-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="f8392-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="f8392-123">Opção ignorar nomes de host personalizados</span><span class="sxs-lookup"><span data-stu-id="f8392-123">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="f8392-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="f8392-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="f8392-125">Opção ignorar controle de origem</span><span class="sxs-lookup"><span data-stu-id="f8392-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="f8392-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8392-126">-Name</span></span>
<span data-ttu-id="f8392-127">Nome do webapp</span><span class="sxs-lookup"><span data-stu-id="f8392-127">Webapp Name</span></span>

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

### <span data-ttu-id="f8392-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8392-128">-ResourceGroupName</span></span>
<span data-ttu-id="f8392-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f8392-129">Resource Group Name</span></span>

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

### <span data-ttu-id="f8392-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="f8392-130">-Slot</span></span>
<span data-ttu-id="f8392-131">Nome do slot do webapp</span><span class="sxs-lookup"><span data-stu-id="f8392-131">Webapp Slot Name</span></span>

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

### <span data-ttu-id="f8392-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="f8392-132">-SourceWebApp</span></span>
<span data-ttu-id="f8392-133">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="f8392-133">Source WebApp Object</span></span>

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

### <span data-ttu-id="f8392-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8392-134">-AsJob</span></span>
<span data-ttu-id="f8392-135">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f8392-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8392-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8392-136">CommonParameters</span></span>
<span data-ttu-id="f8392-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8392-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8392-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8392-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8392-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8392-139">INPUTS</span></span>

### <span data-ttu-id="f8392-140">Instalação</span><span class="sxs-lookup"><span data-stu-id="f8392-140">Site</span></span>
<span data-ttu-id="f8392-141">O parâmetro ' SourceWebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="f8392-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f8392-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8392-142">OUTPUTS</span></span>

## <span data-ttu-id="f8392-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8392-143">NOTES</span></span>

## <span data-ttu-id="f8392-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8392-144">RELATED LINKS</span></span>

[<span data-ttu-id="f8392-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8392-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f8392-146">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8392-146">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="f8392-147">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8392-147">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="f8392-148">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8392-148">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="f8392-149">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8392-149">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="f8392-150">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8392-150">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="f8392-151">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f8392-151">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="f8392-152">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f8392-152">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
