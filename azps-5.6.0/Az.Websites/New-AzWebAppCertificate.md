---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 8e4ed309d4109ecfe230a522a65054213ae32049
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887928"
---
# <span data-ttu-id="790fc-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="790fc-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="790fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="790fc-102">SYNOPSIS</span></span>
<span data-ttu-id="790fc-103">Cria um certificado gerenciado do serviço de aplicativo para um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="790fc-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="790fc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="790fc-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="790fc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="790fc-105">DESCRIPTION</span></span>
<span data-ttu-id="790fc-106">O cmdlet **New-AzWebAppCertificate** cria um Certificado Gerenciado do Serviço de Aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="790fc-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="790fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="790fc-107">EXAMPLES</span></span>

### <span data-ttu-id="790fc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="790fc-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="790fc-109">Este comando cria um Certificado Gerenciado do Serviço de Aplicativo para o WebApp determinado</span><span class="sxs-lookup"><span data-stu-id="790fc-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="790fc-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="790fc-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="790fc-111">Este comando cria um Certificado Gerenciado do Serviço de Aplicativo e se vincula ao Slot WebApp determinado.</span><span class="sxs-lookup"><span data-stu-id="790fc-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="790fc-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="790fc-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="790fc-113">Este comando cria um Certificado Gerenciado do Serviço de Aplicativo e se vincula ao WebApp determinado.</span><span class="sxs-lookup"><span data-stu-id="790fc-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="790fc-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="790fc-114">PARAMETERS</span></span>

### <span data-ttu-id="790fc-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="790fc-115">-AddBinding</span></span>
<span data-ttu-id="790fc-116">Para adicionar o certificado criado ao WebApp/slot.</span><span class="sxs-lookup"><span data-stu-id="790fc-116">To add the created certificate to WebApp/slot.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="790fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790fc-117">-DefaultProfile</span></span>
<span data-ttu-id="790fc-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="790fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="790fc-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="790fc-119">-HostName</span></span>
<span data-ttu-id="790fc-120">Nomes de host personalizados associados ao aplicativo Web/slot.</span><span class="sxs-lookup"><span data-stu-id="790fc-120">Custom hostnames associated with web app/slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="790fc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="790fc-121">-Name</span></span>
<span data-ttu-id="790fc-122">O nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="790fc-122">The name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="790fc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="790fc-123">-ResourceGroupName</span></span>
<span data-ttu-id="790fc-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="790fc-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="790fc-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="790fc-125">-Slot</span></span>
<span data-ttu-id="790fc-126">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="790fc-126">The name of the web app slot.</span></span>

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

### <span data-ttu-id="790fc-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="790fc-127">-SslState</span></span>
<span data-ttu-id="790fc-128">Opção de estado Ssl.</span><span class="sxs-lookup"><span data-stu-id="790fc-128">Ssl state option.</span></span>
<span data-ttu-id="790fc-129">Use 'SniEnabled' ou 'IpBasedEnabled'.</span><span class="sxs-lookup"><span data-stu-id="790fc-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="790fc-130">A opção padrão é 'SniEnabled'.</span><span class="sxs-lookup"><span data-stu-id="790fc-130">Default option is 'SniEnabled'.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="790fc-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="790fc-131">-WebAppName</span></span>
<span data-ttu-id="790fc-132">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="790fc-132">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="790fc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790fc-133">CommonParameters</span></span>
<span data-ttu-id="790fc-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="790fc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790fc-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="790fc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790fc-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="790fc-136">INPUTS</span></span>

### <span data-ttu-id="790fc-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="790fc-137">None</span></span>

## <span data-ttu-id="790fc-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="790fc-138">OUTPUTS</span></span>

### <span data-ttu-id="790fc-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="790fc-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="790fc-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="790fc-140">NOTES</span></span>

## <span data-ttu-id="790fc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="790fc-141">RELATED LINKS</span></span>
[<span data-ttu-id="790fc-142">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="790fc-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)