---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 3ed7bd25c394c2bef5cb3636a4f8c238f45a3558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426864"
---
# <span data-ttu-id="da449-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="da449-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="da449-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da449-102">SYNOPSIS</span></span>
<span data-ttu-id="da449-103">Definir nomes de configuração do slot para aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="da449-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da449-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da449-104">SYNTAX</span></span>

### <span data-ttu-id="da449-105">Eles</span><span class="sxs-lookup"><span data-stu-id="da449-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da449-106">S2</span><span class="sxs-lookup"><span data-stu-id="da449-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da449-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da449-107">DESCRIPTION</span></span>
<span data-ttu-id="da449-108">O cmdlet **set-AzureRmWebAppSlotConfigName** marca as configurações do aplicativo e as cadeias de conexão como configurações do slot</span><span class="sxs-lookup"><span data-stu-id="da449-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="da449-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da449-109">EXAMPLES</span></span>

### <span data-ttu-id="da449-110">1:</span><span class="sxs-lookup"><span data-stu-id="da449-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="da449-111">Esse comando Remove todas as configurações do aplicativo e cadeias de conexão do aplicativo Web ContosoWebApp associados ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="da449-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="da449-112">OS</span><span class="sxs-lookup"><span data-stu-id="da449-112">PARAMETERS</span></span>

### <span data-ttu-id="da449-113">-AppSettingnames</span><span class="sxs-lookup"><span data-stu-id="da449-113">-AppSettingNames</span></span>
<span data-ttu-id="da449-114">Matriz de cadeias de nomes de configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="da449-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da449-115">-ConnectionStringnames</span><span class="sxs-lookup"><span data-stu-id="da449-115">-ConnectionStringNames</span></span>
<span data-ttu-id="da449-116">Matriz de cadeias de nomes de cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="da449-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da449-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="da449-117">-Name</span></span>
<span data-ttu-id="da449-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="da449-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da449-119">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="da449-119">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="da449-120">Opção remover todos os nomes de configuração do aplicativo</span><span class="sxs-lookup"><span data-stu-id="da449-120">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da449-121">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="da449-121">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="da449-122">Opção remover todos os nomes de cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="da449-122">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da449-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da449-123">-ResourceGroupName</span></span>
<span data-ttu-id="da449-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="da449-124">Resource Group Name</span></span>

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

### <span data-ttu-id="da449-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="da449-125">-WebApp</span></span>
<span data-ttu-id="da449-126">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="da449-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da449-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da449-127">-DefaultProfile</span></span>
<span data-ttu-id="da449-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da449-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da449-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da449-129">CommonParameters</span></span>
<span data-ttu-id="da449-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da449-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da449-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da449-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da449-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da449-132">INPUTS</span></span>

### <span data-ttu-id="da449-133">Instalação</span><span class="sxs-lookup"><span data-stu-id="da449-133">Site</span></span>
<span data-ttu-id="da449-134">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="da449-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="da449-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da449-135">OUTPUTS</span></span>

## <span data-ttu-id="da449-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da449-136">NOTES</span></span>

## <span data-ttu-id="da449-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da449-137">RELATED LINKS</span></span>

