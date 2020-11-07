---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 103c5e75b433fcb585113e8ef6bc89aab1f82d7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785408"
---
# <span data-ttu-id="78710-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="78710-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="78710-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78710-102">SYNOPSIS</span></span>
<span data-ttu-id="78710-103">Obtém uma associação SSL do certificado do aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="78710-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78710-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78710-104">SYNTAX</span></span>

### <span data-ttu-id="78710-105">Eles</span><span class="sxs-lookup"><span data-stu-id="78710-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78710-106">S2</span><span class="sxs-lookup"><span data-stu-id="78710-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78710-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78710-107">DESCRIPTION</span></span>
<span data-ttu-id="78710-108">O cmdlet **Get-AzureRmWebAppSSLBinding** Obtém uma associação SSL (Secure Sockets Layer) para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="78710-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="78710-109">Associações SSL são usadas para associar um aplicativo Web a um certificado carregado.</span><span class="sxs-lookup"><span data-stu-id="78710-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="78710-110">Os aplicativos Web podem ser associados a vários certificados.</span><span class="sxs-lookup"><span data-stu-id="78710-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="78710-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78710-111">EXAMPLES</span></span>

### <span data-ttu-id="78710-112">Exemplo 1: obter associações SSL para um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="78710-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="78710-113">Esse comando recupera as associações SSL para o aplicativo Web ContosoWebApp, que está associado à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78710-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="78710-114">Exemplo 2: usar uma referência de objeto para obter associações SSL para um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="78710-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="78710-115">Os comandos neste exemplo também obtêm associações SSL para o aplicativo Web ContosoWebApp; Nesse caso, no entanto, uma referência de objeto é usada em vez do nome do aplicativo Web e o nome do grupo de recursos associado.</span><span class="sxs-lookup"><span data-stu-id="78710-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="78710-116">Essa referência de objeto é criada pelo primeiro comando no exemplo, que usa **Get-AzureRmWebApp** para criar uma referência de objeto para o aplicativo Web chamado ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="78710-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="78710-117">Essa referência de objeto é armazenada em uma variável chamada $WebApp.</span><span class="sxs-lookup"><span data-stu-id="78710-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="78710-118">Essa variável, e o cmdlet **Get-AzureRmWebAppSSLBinding** , são então usadas pelo segundo comando para obter as associações SSL.</span><span class="sxs-lookup"><span data-stu-id="78710-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="78710-119">OS</span><span class="sxs-lookup"><span data-stu-id="78710-119">PARAMETERS</span></span>

### <span data-ttu-id="78710-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78710-120">-DefaultProfile</span></span>
<span data-ttu-id="78710-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78710-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78710-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="78710-122">-Name</span></span>
<span data-ttu-id="78710-123">Especifica o nome da Associação SSL.</span><span class="sxs-lookup"><span data-stu-id="78710-123">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="78710-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78710-124">-ResourceGroupName</span></span>
<span data-ttu-id="78710-125">Especifica o nome do grupo de recursos ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="78710-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="78710-126">Não é possível usar o parâmetro *ResourceGroupName* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="78710-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78710-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="78710-127">-Slot</span></span>
<span data-ttu-id="78710-128">Especifica um slot de implantação do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="78710-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="78710-129">Para obter um slot de implantação, use o cmdlet Get-AzureRMWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="78710-129">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78710-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="78710-130">-WebApp</span></span>
<span data-ttu-id="78710-131">Especifica um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="78710-131">Specifies a Web App.</span></span>
<span data-ttu-id="78710-132">Para obter um aplicativo Web, use o cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="78710-132">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78710-133">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="78710-133">-WebAppName</span></span>
<span data-ttu-id="78710-134">Especifica o nome do aplicativo Web do qual este cmdlet obtém associações SSL.</span><span class="sxs-lookup"><span data-stu-id="78710-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="78710-135">Não é possível usar o parâmetro *webappname* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="78710-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78710-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78710-136">CommonParameters</span></span>
<span data-ttu-id="78710-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78710-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78710-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78710-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78710-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78710-139">INPUTS</span></span>

### <span data-ttu-id="78710-140">Instalação</span><span class="sxs-lookup"><span data-stu-id="78710-140">Site</span></span>
<span data-ttu-id="78710-141">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="78710-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="78710-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78710-142">OUTPUTS</span></span>

## <span data-ttu-id="78710-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78710-143">NOTES</span></span>

## <span data-ttu-id="78710-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78710-144">RELATED LINKS</span></span>

[<span data-ttu-id="78710-145">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="78710-145">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="78710-146">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="78710-146">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="78710-147">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="78710-147">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


