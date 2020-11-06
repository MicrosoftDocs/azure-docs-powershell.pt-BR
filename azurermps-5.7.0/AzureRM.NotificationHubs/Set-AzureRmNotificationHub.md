---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
ms.openlocfilehash: e035cb24c6341eb6d5b3d8aba5cd86b67fdafca2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441297"
---
# <span data-ttu-id="12c66-101">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="12c66-101">Set-AzureRmNotificationHub</span></span>

## <span data-ttu-id="12c66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12c66-102">SYNOPSIS</span></span>
<span data-ttu-id="12c66-103">Define valores de propriedade para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="12c66-103">Sets property values for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12c66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12c66-104">SYNTAX</span></span>

### <span data-ttu-id="12c66-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="12c66-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12c66-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="12c66-106">NotificationHubParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12c66-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12c66-107">DESCRIPTION</span></span>
<span data-ttu-id="12c66-108">O cmdlet **set-AzureRmNotificationHub** modifica os valores de propriedade de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="12c66-108">The **Set-AzureRmNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>

<span data-ttu-id="12c66-109">Você pode modificar um valor de propriedade de Hub de notificação de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="12c66-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="12c66-110">Para um, você pode criar uma instância do objeto **NotificationHubAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que o novo hub possua.</span><span class="sxs-lookup"><span data-stu-id="12c66-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="12c66-111">Isso pode ser feito por meio do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="12c66-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="12c66-112">Em seguida, você pode copiar esses valores de propriedade para o seu hub por meio do parâmetro *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="12c66-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="12c66-113">Você também pode criar um arquivo JSON (JavaScript Object Notation) que contenha os valores de configuração relevantes e, em seguida, aplicar esses valores por meio do parâmetro *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="12c66-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="12c66-114">Um arquivo JSON é um arquivo de texto que usa sintaxe semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="12c66-114">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="12c66-115">{</span><span class="sxs-lookup"><span data-stu-id="12c66-115">{</span></span>  
    <span data-ttu-id="12c66-116">"Nome": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="12c66-116">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="12c66-117">"Local": "Oeste EUA",</span><span class="sxs-lookup"><span data-stu-id="12c66-117">"Location": "West US",</span></span>  
<span data-ttu-id="12c66-118">}</span><span class="sxs-lookup"><span data-stu-id="12c66-118">}</span></span>

<span data-ttu-id="12c66-119">Quando usado em conjunto com o cmdlet **set-AzureRmNotificationHub** , o exemplo JSON anterior define o valor de localização de um hub de notificação chamado ContosoNotificationHub para Oeste EUA.</span><span class="sxs-lookup"><span data-stu-id="12c66-119">When used in conjunction with the **Set-AzureRmNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="12c66-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12c66-120">EXAMPLES</span></span>

### <span data-ttu-id="12c66-121">Exemplo 1: modificar os valores de propriedade de um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="12c66-121">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="12c66-122">Esse comando modifica os valores de propriedade para um hub de notificação encontrado no namespace ContosoNamespace e os atribui à ContosoNotificationsGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12c66-122">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="12c66-123">Os valores de propriedade, bem como o nome do hub a ser modificado, não são especificados no comando.</span><span class="sxs-lookup"><span data-stu-id="12c66-123">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="12c66-124">Em vez disso, essas informações estão contidas no arquivo de entrada C:\Configuration\Hubs.js.</span><span class="sxs-lookup"><span data-stu-id="12c66-124">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="12c66-125">OS</span><span class="sxs-lookup"><span data-stu-id="12c66-125">PARAMETERS</span></span>

### <span data-ttu-id="12c66-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c66-126">-DefaultProfile</span></span>
<span data-ttu-id="12c66-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="12c66-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12c66-128">-Force</span><span class="sxs-lookup"><span data-stu-id="12c66-128">-Force</span></span>
<span data-ttu-id="12c66-129">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="12c66-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="12c66-130">-InputFile</span><span class="sxs-lookup"><span data-stu-id="12c66-130">-InputFile</span></span>
<span data-ttu-id="12c66-131">Especifica o caminho para um arquivo JSON que contém informações de configuração para o Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="12c66-131">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c66-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="12c66-132">-Namespace</span></span>
<span data-ttu-id="12c66-133">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="12c66-133">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="12c66-134">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="12c66-134">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="12c66-135">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="12c66-135">-NotificationHubObj</span></span>
<span data-ttu-id="12c66-136">Especifica o objeto **NotificationHubAttributes** que contém as informações de configuração para o Hub que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="12c66-136">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c66-137">-Resource</span><span class="sxs-lookup"><span data-stu-id="12c66-137">-ResourceGroup</span></span>
<span data-ttu-id="12c66-138">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="12c66-138">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="12c66-139">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="12c66-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="12c66-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12c66-140">-Confirm</span></span>
<span data-ttu-id="12c66-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12c66-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c66-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12c66-142">-WhatIf</span></span>
<span data-ttu-id="12c66-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12c66-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12c66-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12c66-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c66-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c66-145">CommonParameters</span></span>
<span data-ttu-id="12c66-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c66-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c66-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c66-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c66-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12c66-148">INPUTS</span></span>

### <span data-ttu-id="12c66-149">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="12c66-149">None</span></span>
<span data-ttu-id="12c66-150">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="12c66-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12c66-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12c66-151">OUTPUTS</span></span>

### <span data-ttu-id="12c66-152">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="12c66-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="12c66-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12c66-153">NOTES</span></span>

## <span data-ttu-id="12c66-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12c66-154">RELATED LINKS</span></span>

[<span data-ttu-id="12c66-155">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="12c66-155">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="12c66-156">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="12c66-156">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="12c66-157">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="12c66-157">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

