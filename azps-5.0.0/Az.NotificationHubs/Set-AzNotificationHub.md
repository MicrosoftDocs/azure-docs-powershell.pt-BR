---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 3dc4a81731f42ce6a27ae5d23fb7c81af76cf789
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281995"
---
# <span data-ttu-id="35b4c-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="35b4c-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="35b4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="35b4c-103">Define valores de propriedade para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="35b4c-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="35b4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35b4c-104">SYNTAX</span></span>

### <span data-ttu-id="35b4c-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="35b4c-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35b4c-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="35b4c-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35b4c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35b4c-107">DESCRIPTION</span></span>
<span data-ttu-id="35b4c-108">O cmdlet **set-AzNotificationHub** modifica os valores de propriedade de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="35b4c-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="35b4c-109">Você pode modificar um valor de propriedade de Hub de notificação de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="35b4c-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="35b4c-110">Para um, você pode criar uma instância do objeto **NotificationHubAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que o novo hub possua.</span><span class="sxs-lookup"><span data-stu-id="35b4c-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="35b4c-111">Isso pode ser feito por meio do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="35b4c-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="35b4c-112">Em seguida, você pode copiar esses valores de propriedade para o seu hub por meio do parâmetro *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="35b4c-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="35b4c-113">Você também pode criar um arquivo JSON (JavaScript Object Notation) que contenha os valores de configuração relevantes e, em seguida, aplicar esses valores por meio do parâmetro *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="35b4c-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="35b4c-114">Um arquivo JSON é um arquivo de texto que usa sintaxe semelhante à seguinte: {</span><span class="sxs-lookup"><span data-stu-id="35b4c-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="35b4c-115">"Nome": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="35b4c-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="35b4c-116">"Local": "Oeste EUA",</span><span class="sxs-lookup"><span data-stu-id="35b4c-116">"Location": "West US",</span></span>  
<span data-ttu-id="35b4c-117">} Quando usado em conjunto com o cmdlet **set-AzNotificationHub** , o exemplo JSON anterior define o valor de localização de um hub de notificação chamado ContosoNotificationHub para Oeste EUA.</span><span class="sxs-lookup"><span data-stu-id="35b4c-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="35b4c-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35b4c-118">EXAMPLES</span></span>

### <span data-ttu-id="35b4c-119">Exemplo 1: modificar os valores de propriedade de um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="35b4c-119">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="35b4c-120">Esse comando modifica os valores de propriedade para um hub de notificação encontrado no namespace ContosoNamespace e os atribui à ContosoNotificationsGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35b4c-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="35b4c-121">Os valores de propriedade, bem como o nome do hub a ser modificado, não são especificados no comando.</span><span class="sxs-lookup"><span data-stu-id="35b4c-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="35b4c-122">Em vez disso, essas informações estão contidas no arquivo de entrada C:\Configuration\Hubs.js.</span><span class="sxs-lookup"><span data-stu-id="35b4c-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="35b4c-123">OS</span><span class="sxs-lookup"><span data-stu-id="35b4c-123">PARAMETERS</span></span>

### <span data-ttu-id="35b4c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b4c-124">-DefaultProfile</span></span>
<span data-ttu-id="35b4c-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="35b4c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35b4c-126">-Force</span><span class="sxs-lookup"><span data-stu-id="35b4c-126">-Force</span></span>
<span data-ttu-id="35b4c-127">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="35b4c-127">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b4c-128">-InputFile</span><span class="sxs-lookup"><span data-stu-id="35b4c-128">-InputFile</span></span>
<span data-ttu-id="35b4c-129">Especifica o caminho para um arquivo JSON que contém informações de configuração para o Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="35b4c-129">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b4c-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="35b4c-130">-Namespace</span></span>
<span data-ttu-id="35b4c-131">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="35b4c-131">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="35b4c-132">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="35b4c-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="35b4c-133">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="35b4c-133">-NotificationHubObj</span></span>
<span data-ttu-id="35b4c-134">Especifica o objeto **NotificationHubAttributes** que contém as informações de configuração para o Hub que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="35b4c-134">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b4c-135">-Resource</span><span class="sxs-lookup"><span data-stu-id="35b4c-135">-ResourceGroup</span></span>
<span data-ttu-id="35b4c-136">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="35b4c-136">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="35b4c-137">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="35b4c-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b4c-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35b4c-138">-Confirm</span></span>
<span data-ttu-id="35b4c-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35b4c-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b4c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35b4c-140">-WhatIf</span></span>
<span data-ttu-id="35b4c-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35b4c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35b4c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35b4c-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b4c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b4c-143">CommonParameters</span></span>
<span data-ttu-id="35b4c-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b4c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b4c-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35b4c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b4c-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35b4c-146">INPUTS</span></span>

### <span data-ttu-id="35b4c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="35b4c-147">System.String</span></span>

## <span data-ttu-id="35b4c-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35b4c-148">OUTPUTS</span></span>

### <span data-ttu-id="35b4c-149">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="35b4c-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="35b4c-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35b4c-150">NOTES</span></span>

## <span data-ttu-id="35b4c-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35b4c-151">RELATED LINKS</span></span>

[<span data-ttu-id="35b4c-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="35b4c-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="35b4c-153">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="35b4c-153">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="35b4c-154">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="35b4c-154">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


