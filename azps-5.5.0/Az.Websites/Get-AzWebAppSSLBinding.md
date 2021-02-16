---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118506"
---
# <span data-ttu-id="5a32d-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="5a32d-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="5a32d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a32d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a32d-103">Obtém uma vinculação SSL de certificado do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5a32d-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="5a32d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a32d-104">SYNTAX</span></span>

### <span data-ttu-id="5a32d-105">S1</span><span class="sxs-lookup"><span data-stu-id="5a32d-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a32d-106">S2</span><span class="sxs-lookup"><span data-stu-id="5a32d-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a32d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a32d-107">DESCRIPTION</span></span>
<span data-ttu-id="5a32d-108">O cmdlet **Get-AzWebAppSSLBinding** obtém uma encadernação SSL (Secure Sockets Layer) para um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5a32d-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="5a32d-109">As associações SSL são usadas para associar um Web App a um certificado carregado.</span><span class="sxs-lookup"><span data-stu-id="5a32d-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="5a32d-110">Os Web Apps podem ser vinculados a vários certificados.</span><span class="sxs-lookup"><span data-stu-id="5a32d-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="5a32d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5a32d-111">EXAMPLES</span></span>

### <span data-ttu-id="5a32d-112">Exemplo 1: Obter encadernações SSL para um Web App</span><span class="sxs-lookup"><span data-stu-id="5a32d-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="5a32d-113">Esse comando recupera as vinculações SSL do Web App ContosoWebApp, que está associado ao grupo de recursos ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5a32d-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="5a32d-114">Exemplo 2: Usar uma referência de objeto para obter encadernações SSL para um Web App</span><span class="sxs-lookup"><span data-stu-id="5a32d-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="5a32d-115">Os comandos neste exemplo também têm as ligações SSL para o Web App ContosoWebApp; nesse caso, no entanto, uma referência de objeto é usada em vez do nome do Web App e do nome do grupo de recursos associado.</span><span class="sxs-lookup"><span data-stu-id="5a32d-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="5a32d-116">Essa referência de objeto é criada pelo primeiro comando no exemplo, que usa **Get-AzWebApp** para criar uma referência de objeto ao Web App chamada ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="5a32d-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="5a32d-117">Essa referência de objeto é armazenada em uma variável chamada $WebApp.</span><span class="sxs-lookup"><span data-stu-id="5a32d-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="5a32d-118">Essa variável e o cmdlet **Get-AzWebAppSSLBinding** são usados pelo segundo comando para obter as ligações SSL.</span><span class="sxs-lookup"><span data-stu-id="5a32d-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="5a32d-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a32d-119">PARAMETERS</span></span>

### <span data-ttu-id="5a32d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a32d-120">-DefaultProfile</span></span>
<span data-ttu-id="5a32d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5a32d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a32d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a32d-122">-Name</span></span>
<span data-ttu-id="5a32d-123">Especifica o nome da associação SSL.</span><span class="sxs-lookup"><span data-stu-id="5a32d-123">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="5a32d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a32d-124">-ResourceGroupName</span></span>
<span data-ttu-id="5a32d-125">Especifica o nome do grupo de recursos ao que o certificado foi atribuído.</span><span class="sxs-lookup"><span data-stu-id="5a32d-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="5a32d-126">Você não pode usar *o parâmetro ResourceGroupName* e o parâmetro *WebApp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="5a32d-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a32d-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="5a32d-127">-Slot</span></span>
<span data-ttu-id="5a32d-128">Especifica um slot de implantação do Web App.</span><span class="sxs-lookup"><span data-stu-id="5a32d-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="5a32d-129">Para obter um slot de implantação, use Get-AzWebAppSlot cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a32d-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a32d-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5a32d-130">-WebApp</span></span>
<span data-ttu-id="5a32d-131">Especifica um Web App.</span><span class="sxs-lookup"><span data-stu-id="5a32d-131">Specifies a Web App.</span></span>
<span data-ttu-id="5a32d-132">Para obter um Aplicativo Web, use o Get-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a32d-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a32d-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="5a32d-133">-WebAppName</span></span>
<span data-ttu-id="5a32d-134">Especifica o nome do Web App de onde este cmdlet obtém encadernações SSL.</span><span class="sxs-lookup"><span data-stu-id="5a32d-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="5a32d-135">Você não pode usar o parâmetro *WebAppName* e o parâmetro *WebApp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="5a32d-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a32d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a32d-136">CommonParameters</span></span>
<span data-ttu-id="5a32d-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a32d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a32d-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a32d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a32d-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="5a32d-139">INPUTS</span></span>

### <span data-ttu-id="5a32d-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5a32d-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5a32d-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="5a32d-141">OUTPUTS</span></span>

### <span data-ttu-id="5a32d-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="5a32d-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="5a32d-143">Notas</span><span class="sxs-lookup"><span data-stu-id="5a32d-143">NOTES</span></span>

## <span data-ttu-id="5a32d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a32d-144">RELATED LINKS</span></span>

[<span data-ttu-id="5a32d-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="5a32d-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="5a32d-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="5a32d-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="5a32d-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5a32d-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


