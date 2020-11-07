---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: ab00a1fbafc446affd30d7ae06dd0d48f0f0d04d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776060"
---
# <span data-ttu-id="8b326-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="8b326-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="8b326-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b326-102">SYNOPSIS</span></span>
<span data-ttu-id="8b326-103">Definir nomes de configuração do slot para aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="8b326-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="8b326-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b326-104">SYNTAX</span></span>

### <span data-ttu-id="8b326-105">Eles</span><span class="sxs-lookup"><span data-stu-id="8b326-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b326-106">S2</span><span class="sxs-lookup"><span data-stu-id="8b326-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b326-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b326-107">DESCRIPTION</span></span>
<span data-ttu-id="8b326-108">O cmdlet **set-AzWebAppSlotConfigName** marca as configurações do aplicativo e as cadeias de conexão como configurações do slot</span><span class="sxs-lookup"><span data-stu-id="8b326-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="8b326-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b326-109">EXAMPLES</span></span>

### <span data-ttu-id="8b326-110">1:</span><span class="sxs-lookup"><span data-stu-id="8b326-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="8b326-111">Esse comando Remove todas as configurações do aplicativo e cadeias de conexão do aplicativo Web ContosoWebApp associados ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="8b326-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="8b326-112">OS</span><span class="sxs-lookup"><span data-stu-id="8b326-112">PARAMETERS</span></span>

### <span data-ttu-id="8b326-113">-AppSettingnames</span><span class="sxs-lookup"><span data-stu-id="8b326-113">-AppSettingNames</span></span>
<span data-ttu-id="8b326-114">Matriz de cadeias de nomes de configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="8b326-114">App Settings Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b326-115">-ConnectionStringnames</span><span class="sxs-lookup"><span data-stu-id="8b326-115">-ConnectionStringNames</span></span>
<span data-ttu-id="8b326-116">Matriz de cadeias de nomes de cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="8b326-116">Connection String Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b326-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b326-117">-DefaultProfile</span></span>
<span data-ttu-id="8b326-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b326-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b326-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b326-119">-Name</span></span>
<span data-ttu-id="8b326-120">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="8b326-120">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b326-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="8b326-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="8b326-122">Opção remover todos os nomes de configuração do aplicativo</span><span class="sxs-lookup"><span data-stu-id="8b326-122">Remove All App Setting Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b326-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="8b326-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="8b326-124">Opção remover todos os nomes de cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="8b326-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="8b326-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b326-125">-ResourceGroupName</span></span>
<span data-ttu-id="8b326-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8b326-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8b326-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8b326-127">-WebApp</span></span>
<span data-ttu-id="8b326-128">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="8b326-128">WebApp Object</span></span>

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

### <span data-ttu-id="8b326-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b326-129">CommonParameters</span></span>
<span data-ttu-id="8b326-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b326-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b326-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b326-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b326-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b326-132">INPUTS</span></span>

### <span data-ttu-id="8b326-133">Instalação</span><span class="sxs-lookup"><span data-stu-id="8b326-133">Site</span></span>
<span data-ttu-id="8b326-134">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="8b326-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8b326-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b326-135">OUTPUTS</span></span>

## <span data-ttu-id="8b326-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b326-136">NOTES</span></span>

## <span data-ttu-id="8b326-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b326-137">RELATED LINKS</span></span>

